# Google — Laboratório de ideias com IA

## Avaliação posterior

Após a escolha e exportação, o usuário considerou este resultado abaixo da personalidade visual dos modelos PODS e Vinteum. O caso demonstra a execução técnica da versão inicial da skill, mas não é referência estética aprovada. A skill foi revista para começar por seleção visual de referências e avaliar a integração entre atmosfera, grafismos, tipografia e espaço antes da finalização.

Status: **proposta 01 — Editorial aberto aprovada e finalizada**. A proposta 02 permanece apenas como alternativa histórica.

Evento fictício, usado exclusivamente como exemplo de design para avaliação. Não existe confirmação de realização, participação, apoio ou emissão pela Google. Os HTML incluem identificação visível de estudo fictício, sem vínculo ou endosso e sem validade.

## Pesquisa de marca

**Documentado:** o [Partner Marketing Hub](https://partnermarketinghub.withgoogle.com/brands/google/branding-guidelines/how-to-show-googles-brand/) orienta preservar o logo, seu espaço de proteção e a apresentação precisa do papel da Google. A aplicação das marcas não deve sugerir endosso inexistente. O logo colorido usa fundo branco. Este estudo não constitui aprovação de uso comercial.

**Documentado:** [Google Design — Making Google Sans Flex](https://design.google/library/google-sans-flex-font) apresenta a evolução da família e sua disponibilização como código aberto. Usamos Google Sans localmente, com a licença SIL OFL em `assets/OFL.txt`, sem substituir ou redesenhar o wordmark.

**Observado:** [About Google](https://about.google/) combina tipografia sem serifa, áreas abertas, cores de acento e módulos simples. Estas são observações do repertório visual, não um manual para certificados. Paleta desta composição: azul #4285F4, vermelho #EA4335, amarelo #FBBC04 e verde #34A853; azul de texto #1967D2. Os códigos são escolhas deste estudo.

**Proposto:** composição editorial ampla ou sistema lateral modular; formas decorativas autorais em CSS, sem imitar símbolo de produto ou assinatura. Frases de apoio da proposta 02 são texto criativo deste estudo, não slogans oficiais.

## Referências numeradas

1. [About Google](https://about.google/) — repertório de páginas claras, hierarquia sans-serif e áreas generosas. Orienta a abertura e o ritmo da proposta 01.
2. [Google Design — Evolving the Google Identity](https://design.google/library/evolving-google-identity) — relação entre tipografia e geometria. Orienta o vocabulário modular da proposta 02, sem copiar um layout.
3. [Teach For Austria — Szenario Design](https://www.szenario-design.com/teach-for-austria) — referência de certificado encontrada por busca de imagens: separação clara de título, nome e assinatura. Aproveitamos hierarquia e respiro, não cores ou grafismos.
4. [MOSS — Brand identity for landscape studio](https://www.behance.net/gallery/189543675/MOSS-Brand-identity-for-landscape-studio) — referência editorial encontrada por busca de imagens: composição assimétrica, campos alinhados e identificação modular. Inspira estrutura, sem reprodução.

## Propostas

- **01 — Editorial aberto:** título e nome alinhados à esquerda, nome em azul, amplo campo branco e uma linha de quatro cores no rodapé. Tratamento mais institucional.
- **02 — Laboratório modular:** painel lateral azul claro, quatro formas geométricas autorais e conteúdo em coluna. Tratamento mais expressivo, ligado à experimentação.

## Campos e pendências

Nome variável: `[NOME DO PARTICIPANTE]` (elemento `data-field="nome"`).
Sem confirmação: `[DATA DO EVENTO]`, `[MODALIDADE]`, `[CARGA HORÁRIA]`, `[LOCAL]`, `[DATA DE EMISSÃO]`, `[INSTITUIÇÃO EMISSORA]`, `[NOME DO SIGNATÁRIO]` e `[CARGO]`.

Formato: 297 × 210 mm, A4 horizontal, impressão sem margem e texto editável no DOM. Controles de navegação ficam fora da folha e são ocultos na impressão. Logo e fontes são locais para funcionamento offline.

Verificação final: HTML exportado no Chromium com fontes e logo carregados, tamanho CSS da página, fundos habilitados, margens zero e cabeçalhos/rodapés desativados. PDF final com uma página A4 horizontal (841,92 × 594,96 pt), texto selecionável e acentos verificados por extração. PDF renderizado pelo Poppler e inspecionado visualmente; sem cortes ou sobreposições. PNG final derivado desse PDF, 2400 × 1697 px.

Nomes testados: **João Sá** e **Maria Júlia de Albuquerque e Vasconcelos de Oliveira Santos**. O nome curto usa uma linha e o longo usa duas, preservando o corpo e a área de assinatura. Ambos resultaram em PDFs de uma página; os dois PDFs foram renderizados para conferência local antes da publicação.

Entregáveis: `certificado-google.html` (fonte editável, requer `styles.css` e `assets/` ao lado), `certificado-google.pdf` e `certificado-google.png`. Placeholders não confirmados e a identificação de estudo fictício foram preservados. Não houve emissão para participantes reais. O exemplo foi publicado no GitHub após a escolha do usuário.

## Assets e proveniência

- `assets/google-logo.svg`: SVG servido pelo próprio About Google, https://www.gstatic.com/marketing-cms/assets/images/f5/d3/a7f9db7045429cb6dc6be56bdcbe/google-logo-about.svg . Marca registrada da Google; não é um asset licenciado sob OFL.
- `assets/google-sans-0.ttf` a `google-sans-3.ttf`: pesos 400/500/600/700 fornecidos por https://fonts.googleapis.com/css2?family=Google+Sans:wght@400;500;600;700&display=swap . Origem dos binários registrada em `assets/font-source.css`.
- `assets/OFL.txt`: licença do projeto oficial https://github.com/googlefonts/googlesans .
- `assets/google-logo.png`: wordmark oficial auxiliar, https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png . Não utilizado na composição; o SVG do site é a fonte efetiva.
