# Portfólio

Site pessoal de página única, em HTML, CSS e JavaScript — sem framework, sem build,
sem dependências. O arquivo inteiro é o deploy.

**No ar:** <https://adrianoanthonymma16-boop.github.io/portfolio-adriano/>

## O que tem

| Seção | Conteúdo |
| :--- | :--- |
| Sobre | Quem sou e o que faço |
| Habilidades | Stack agrupada por área |
| Projetos | Cards com link para o repositório |
| Contato | Links diretos |

## Detalhes técnicos

**Tokens de design em `:root`** — cor, espaçamento, raio e tipografia definidos como
custom properties, então a troca de tema é uma variável, não uma busca por
hexadecimal no arquivo.

**Contraste revisado para WCAG AA** — o texto do corpo foi elevado de `#666` para
`#a3a3a3` justamente por causa disso. `--texto-dim` existe para legenda e decoração,
e nunca é usado em corpo de texto — a distinção está comentada no CSS.

**Tipografia com papéis distintos** — Cinzel para display, Inter para corpo, JetBrains
Mono para trechos técnicos. Cada fonte carregada com `display=swap`, então o texto
aparece antes da webfont terminar.

**Acessibilidade** — HTML5 semântico com `header`/`main`/`section`, `lang="pt-br"`,
`aria-label` nos ícones decorativos, e `aria-labelledby` ligando cada seção ao seu
título.

**Performance** — zero requisições de JavaScript, zero imagens externas. As fontes
vêm do Google Fonts com `preconnect`; o favicon é um SVG inline em data URI, o que
dispensa um arquivo e uma requisição.

## Rodando localmente

```bash
python3 -m http.server 8000
```

Ou abra o `index.html` direto no navegador — funciona sem servidor.

## Publicando

GitHub Pages serve a branch padrão direto. Para subir: *Settings → Pages → Deploy
from a branch* → `main` / root.

## Licença

MIT
