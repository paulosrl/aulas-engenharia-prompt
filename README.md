# aulas-engenharia-prompt

Projeto para produzir aulas completas em Markdown e convertê-las depois para páginas HTML finais, com entrega 100% offline e publicação pública via GitHub Pages.

## Regra principal

- A fonte oficial de cada aula é o arquivo Markdown em `aulas-md/`.
- A aula deve ser escrita, revisada e considerada completa em `.md` antes de qualquer conversão para HTML.
- O HTML é o produto final de entrega, não o lugar para desenvolver o conteúdo didático.
- Cada HTML final deve ser um arquivo único, abrir localmente no navegador e funcionar sem internet.
- Não usar dependências externas: CDN, fontes remotas, JavaScript remoto, CSS remoto ou imagens hospedadas fora do arquivo final.

## Estrutura do projeto

- `aulas-md/`: textos-fonte das aulas em Markdown.
- `aulas-md/GUIA-APOIO.md`: padrão editorial, regras técnicas e checklist.
- `html/`: arquivos HTML finais, já diagramados e prontos para uso offline.
- `index.html`: página pública de entrada para acesso às aulas pelo GitHub Pages.

Arquivos atuais:

- `aulas-md/aula1.md`: conteúdo-base completo da Aula 1.
- `aulas-md/aula1-pratica.md`: conteúdo-base da prática da Aula 1.
- `aulas-md/aula2.md`: rascunho da Aula 2.
- `aulas-md/aula3.md`: rascunho da Aula 3.
- `aulas-md/aula4.md`: rascunho da Aula 4.
- `html/aula1.html`: versão HTML da Aula 1.
- `html/aula1-pratica-html.html`: versão HTML da prática da Aula 1.

## Acesso público

O repositório deve ficar publicado no GitHub com o nome `aulas-engenharia-prompt`.

Com o GitHub Pages ativo a partir da branch `main`, os HTMLs poderão ser acessados por qualquer pessoa nestes endereços:

- Página inicial: `https://paulosrl.github.io/aulas-engenharia-prompt/`
- Aula 1: `https://paulosrl.github.io/aulas-engenharia-prompt/html/aula1.html`
- Prática da Aula 1: `https://paulosrl.github.io/aulas-engenharia-prompt/html/aula1-pratica-html.html`

## Fluxo obrigatório

1. Criar ou editar a aula em `aulas-md/aulaX.md`.
2. Completar todo o conteúdo didático no Markdown:
   - título definitivo;
   - objetivo;
   - agenda;
   - blocos de conteúdo;
   - exemplos;
   - exercícios;
   - fechamento;
   - observações ou práticas, quando existirem.
3. Revisar o `.md` usando `aulas-md/GUIA-APOIO.md`.
4. Confirmar que o Markdown não é mais placeholder ou rascunho.
5. Só então converter o conteúdo para `html/aulaX.html`.
6. Usar uma aula HTML já validada como base visual.
7. Testar o HTML final localmente, sem internet.

## Quando uma aula Markdown está pronta

Antes de gerar o HTML, confira:

- não há textos genéricos como `Título a definir`, `Texto base`, `Tópico 1` ou instruções de preenchimento;
- a aula tem sequência didática completa, com começo, desenvolvimento e fechamento;
- exemplos e exercícios estão escritos de forma aplicável em sala;
- tabelas, listas e prompts estão claros e sem resíduos técnicos;
- o conteúdo pode ser lido e revisado sem depender do HTML.

## Conversão para HTML

Não há script automatizado de conversão neste repositório. A conversão atual é manual: o conteúdo aprovado em Markdown deve ser aplicado em uma página HTML baseada no layout existente.

## Como os HTMLs são gerados

As páginas HTML não são geradas automaticamente por ferramenta, script ou pipeline de build.

O processo atual é manual:

1. A aula é escrita primeiro em Markdown, dentro de `aulas-md/`.
2. O conteúdo do Markdown é revisado até ficar completo.
3. Depois disso, uma página HTML já pronta é usada como modelo visual.
4. O conteúdo aprovado no Markdown é transferido para o HTML.
5. O HTML final fica em `html/` e deve abrir diretamente no navegador.

Cada HTML é um arquivo completo e independente. Ele inclui o próprio CSS, o próprio JavaScript, a navegação lateral, o tema claro/escuro e os ajustes de responsividade. Isso permite que a aula funcione offline, sem depender de CDN, bibliotecas externas, fontes remotas ou servidor.

Por isso, ao alterar uma aula, a ordem correta é sempre:

1. alterar primeiro o arquivo `.md`;
2. revisar o conteúdo no Markdown;
3. atualizar o HTML correspondente;
4. testar o HTML final localmente.

Regras para a conversão:

- salvar novos HTMLs sempre em `html/`;
- manter CSS e JavaScript embutidos no próprio arquivo;
- preservar navegação lateral, menu mobile, tema e responsividade;
- atualizar links entre aulas e práticas quando necessário;
- atualizar `index.html` com o link público para cada novo HTML final;
- bloquear ou marcar aulas futuras quando ainda não tiverem conteúdo completo;
- garantir que prompts, tabelas e blocos de código não estourem o layout;
- validar em desktop e celular.

## Uso recomendado do codebase

Para criar uma nova aula:

1. Duplique a estrutura de um arquivo em `aulas-md/` ou crie `aulas-md/aulaX.md`.
2. Escreva a aula inteira em Markdown.
3. Revise o conteúdo com o checklist do `GUIA-APOIO.md`.
4. Depois de aprovar o `.md`, crie `html/aulaX.html` a partir de uma aula HTML já validada.
5. Transponha o conteúdo para o HTML sem alterar a lógica visual já validada.
6. Teste o arquivo abrindo diretamente no navegador.

Para alterar uma aula existente:

1. Altere primeiro o arquivo Markdown correspondente.
2. Revise e estabilize o conteúdo no `.md`.
3. Atualize o HTML correspondente apenas depois.
4. Verifique se Markdown e HTML continuam consistentes.

## Controle verificado

- A Aula 1 já possui Markdown e HTML.
- A prática da Aula 1 já possui Markdown e HTML.
- As Aulas 2, 3 e 4 ainda estão como rascunho em Markdown e não devem ser convertidas para HTML final antes de serem completadas.
- A regra operacional deste projeto é: primeiro gerar a aula completa em `.md`; depois converter para HTML offline.
