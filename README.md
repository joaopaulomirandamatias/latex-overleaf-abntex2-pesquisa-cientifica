# LaTeX com Overleaf e abnTeX2: passo a passo (MirandasTech)

Manual em formato de slides (50) para escrever o trabalho acadêmico em LaTeX na pós-graduação: o que é LaTeX e quando vale a pena (o que a evidência diz), Overleaf ou instalação local, anatomia de um documento, comandos do dia a dia, português correto e motores (pdfLaTeX, XeLaTeX, LuaLaTeX); o Overleaf passo a passo sem login (conta, primeiro projeto, editor, galeria de modelos e «Open as Template», modelos brasileiros, enviar e baixar, compartilhar, Track changes e History, planos e preços, erros e logs, IA no Overleaf); o abnTeX2 por dentro (normas atendidas e o aviso sobre as edições vigentes, instalação, o modelo canônico compilado de verdade — classe, pacotes e dados, pré-textuais, textual e pós-textual —, citações e referências com `abntex2cite`, a sequência pdflatex → bibtex → makeindex → pdflatex, artigo e projeto de pesquisa, customizações institucionais e biblatex-abnt, erros comuns); do Zotero ao LaTeX com o Better BibTeX e os scripts (`novo_trabalho.py`, `compilar.sh`, `checar_citacoes.py`), instalação local com o TinyTeX, VS Code + LaTeX Workshop, pandoc para gerar `.docx`, Git para versionar; erros comuns, checklist, glossário com popovers e referências. Capturas reais e datadas (09/09/2026) das páginas públicas do Overleaf e do abnTeX2 e dos modelos compilados localmente; nenhuma captura exigiu login.

**Manual on-line:** https://latex.mirandastech.com.br/ · **PDF:** https://latex.mirandastech.com.br/manual.pdf

Manuais irmãos: **Busca em bases científicas** — https://busca.mirandastech.com.br/ · **Revisão sistemática com PRISMA 2020** — https://prisma.mirandastech.com.br/ · **Zotero** — https://zotero.mirandastech.com.br/ · **Metodologia** — https://metodologia.mirandastech.com.br/ · **Gemini Notebook** — https://notebook.mirandastech.com.br/ · **Uso de IA na pesquisa** — https://manual.mirandastech.com.br/ · **Plugin Pesquisa (Claude e Codex)** — https://plugin.mirandastech.com.br/ · Hub: https://www.mirandastech.com.br/pesquisa

| Pasta | O que há |
|---|---|
| `manual/` | deck HTML autônomo, PDF, fonte do artefato e `fatos_verificados.md` (todas as fontes, versões e compilações conferidas em 09/09/2026) |
| `site/` | o que o servidor serve (`index.html`, `manual.pdf`) |
| `capturas/` | 35 capturas reais, 09/09/2026 (25 telas do Overleaf, abnTeX2, CTAN, TinyTeX, VS Code e ferramentas; 7 páginas dos modelos compilados; 3 figuras de terminal com saídas reais) |
| `scripts/novo_trabalho.py` | cria um projeto a partir do modelo canônico do abnTeX2 com título, autor, orientador, instituição e tipo de trabalho, e compila |
| `scripts/compilar.sh` | `latexmk` com a sequência completa (pdflatex → bibtex → makeindex → pdflatex), `--limpar`, `--xelatex` e `--lualatex` |
| `scripts/checar_citacoes.py` | chaves citadas que faltam no `.bib` e entradas do `.bib` nunca citadas, seguindo `\input` e `\include` |
| `scripts/gerar_deck.py` | regenera HTML e PDF a partir do fonte |
| `skills/latex-overleaf-abntex2/` | skill do agente (cópia sincronizada do plugin Pesquisa MirandasTech) |
| `Dockerfile` · `Caddyfile` · `railway.json` | deploy estático (Caddy) |
| `.github/workflows/verificar.yml` | CI: integridade do deck e capturas referenciadas |

## Os manuais juntos
Este manual cobre a **escrita em LaTeX**: do modelo do abnTeX2 ao PDF com as referências certas. A biblioteca vem do Zotero (`zotero-pesquisa-cientifica`) pelo Better BibTeX; a busca e a revisão que alimentam as citações estão nos manuais de busca (`busca-bases-pesquisa-cientifica`) e de revisão sistemática (`revisao-sistematica-pesquisa-cientifica`). No plugin **Pesquisa MirandasTech** (`pesquisa-mirandastech`), a skill `latex-overleaf-abntex2` conduz a fase 8 «Escrita ABNT» com os três scripts; ela nunca faz login no Overleaf, não altera o `.bib` sem mostrar a diferença e avisa que o abnTeX2 1.9.7 implementa edições das normas anteriores às vigentes, a conferir com a biblioteca da instituição.

## Como citar
MATIAS, J. P. M. *LaTeX com Overleaf e abnTeX2: passo a passo.* MirandasTech, v1.0, set. 2026. CC BY 4.0.

## Declaração de uso de IA
Escrito com assistência de IA (Claude, Anthropic) na estruturação, redação, automação das capturas e execução dos scripts e das compilações. Versões, nomes de botões, planos e preços, normas e referências conferidos nas fontes oficiais e em compilações reais em 09/09/2026 (lista em `manual/fatos_verificados.md`); nenhuma captura foi feita com login. O autor responde integralmente pelo conteúdo. Overleaf, abnTeX2, CTAN, TeX Live, TinyTeX, Zotero, Better BibTeX, Microsoft e os demais serviços citados são marcas e projetos de terceiros; este manual não tem vínculo com eles.
