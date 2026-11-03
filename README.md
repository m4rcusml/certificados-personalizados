# Certificados personalizados

Skill para Codex que transforma a identidade visual de uma empresa em um template de certificado próprio, por meio de pesquisa, referências, propostas em HTML e refinamento com o usuário.

O objetivo não é trocar o logo de um diploma pronto: é produzir certificados coerentes com cada marca e diferentes entre si. A abordagem foi consolidada a partir de dois projetos, PODS e Vinteum, documentados em [estudos de composição](#exemplos).

## O que ela faz

- Pesquisa manuais, logos, fontes e materiais oficiais, distinguindo regras documentadas de observações e decisões de design.
- Busca referências de certificados e composição, inclusive no Pinterest quando acessível.
- Apresenta direções visuais, incorpora escolhas e preserva os elementos aprovados durante ajustes pontuais.
- Cria a prévia em HTML/CSS e prepara o template para nomes e outros campos variáveis.
- Orienta a verificação e exportação em PDF/PNG, ou PPTX quando solicitado.

A skill é um conjunto de instruções e referências. Não é um aplicativo, renderizador ou gerador por linha de comando. Não exige Canva e não inclui APIs, credenciais, listas reais de participantes, fontes comerciais ou pacotes oficiais de marca.

## Instalação no Codex

Baixe ou clone este repositório e copie a pasta inteira para o diretório de skills, mantendo `SKILL.md` diretamente dentro de `certificados-personalizados`.

**Windows / PowerShell**, a partir da pasta que contém o clone:

```powershell
$skillRoot = if ($env:CODEX_HOME) { Join-Path $env:CODEX_HOME 'skills' } else { Join-Path $env:USERPROFILE '.codex/skills' }
$destination = Join-Path $skillRoot 'certificados-personalizados'
if (Test-Path -LiteralPath $destination) { throw 'A skill já existe. Revise antes de substituir.' }
New-Item -ItemType Directory -Force -Path $skillRoot | Out-Null
Copy-Item -LiteralPath './certificados-personalizados' -Destination $destination -Recurse
```

**macOS / Linux**, a partir da pasta que contém o clone:

```bash
skill_root="${CODEX_HOME:-$HOME/.codex}/skills"
mkdir -p "$skill_root"
test ! -e "$skill_root/certificados-personalizados" && cp -R ./certificados-personalizados "$skill_root/"
```

Abra uma nova conversa no Codex após instalar. Se a skill não aparecer, reinicie o aplicativo. Ela pode ser selecionada automaticamente pelo contexto ou chamada explicitamente com `$certificados-personalizados`.

## Como usar

### Começar um certificado

```text
Use $certificados-personalizados para criar um template de participação
para o evento [TÍTULO], baseado na identidade visual da [EMPRESA].
Pesquise o site [URL] e materiais oficiais. Busque referências e apresente
duas propostas em HTML A4 horizontal antes de finalizar.
O nome será variável. Reserve um campo de assinatura de [NOME/CARGO].
Mantenha placeholders para informações ainda não confirmadas.
```

Informe os dados disponíveis: empresa/site, evento, data e local, modalidade, carga horária validada, instituições, signatários e formatos desejados. Não é necessário ter todos os dados para começar a direção visual.

### Refinar uma proposta

```text
Gostei da proposta 2. Mantenha a tipografia e o fundo, mova os logos para
os cantos superiores e reserve mais espaço para nomes longos.
```

```text
Quero mais identidade da empresa. Explore os símbolos e a composição
dos materiais oficiais, com uma direção diferente do certificado anterior.
```

### Aprovar e exportar

```text
Template aprovado. Teste nomes curtos e longos e entregue HTML, PDF e PNG.
Confira o PDF renderizado antes de entregar. Não faça upload externo.
```

Emissão por CSV, envio ao Drive e PPTX são pedidos posteriores opcionais. A skill não presume essas ações nem garante equivalência entre HTML e PowerPoint sem conferência.

## Ferramentas e limites

Pesquisa requer acesso à web. Pinterest autenticado depende de uma ferramenta de navegador autorizada; uma conta conectada não garante que o runtime consiga acessá-la. A prévia exige navegador, e PDF/PNG exigem exportação/renderização disponíveis no ambiente. Codex deve usar as skills especializadas de PDF, apresentações e design quando disponíveis e pertinentes.

As fontes e logos são obtidos por projeto, observando origem, licença e permissões. Se um recurso não puder ser usado, a skill orienta uma substituição declarada ou um espaço identificado. O certificado não inventa assinaturas, autenticação, carga horária ou garantia de aproveitamento acadêmico.

## Exemplos

- [PODS](assets/exemplos/pods/decisoes.md): fundo claro, contraste serifado/sem serifa, composição central e grafismos discretos.
- [Vinteum](assets/exemplos/vinteum/decisoes.md): fundo petróleo, Sora, composição à esquerda e interpretação de arcos de energia.

São estudos textuais de decisões, sem certificados nominais ou imagens redistribuídas. Marcas citadas pertencem aos respectivos titulares; este projeto não declara vínculo oficial com elas.

## Estrutura

`SKILL.md` contém o fluxo principal; `references/` aprofunda pesquisa, composição e verificação; `assets/exemplos/` reúne os dois estudos; `agents/openai.yaml` define o nome e o prompt no Codex.

Para validar a estrutura com a ferramenta do skill-creator instalada:

```text
python <caminho-do-skill-creator>/scripts/quick_validate.py <caminho-da-skill>
```

O validador verifica a estrutura, não a qualidade estética. Esta depende de pesquisa, aprovação e inspeção das saídas.
