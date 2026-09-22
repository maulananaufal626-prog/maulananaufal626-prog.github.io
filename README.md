# plenosolucoescontabeis.github.io

Site institucional da **Pleno Contabilidade**, publicado via GitHub Pages em
<https://plenosolucoescontabeis.github.io/>.

## Estrutura

- `index.html` — a página completa (HTML + CSS embutido + um script de ~20 linhas
  para o menu mobile). Sem build, sem dependências externas além das fontes do
  Google Fonts.
- `favicon.svg` — ícone do site (o símbolo da marca).
- `.nojekyll` — desativa o processamento Jekyll do GitHub Pages; os arquivos são
  servidos como estão.
- `Main-html/` — mockup original de design (componente React exportado de uma
  ferramenta visual). É apenas referência; não é publicado nem necessário para o
  site funcionar.

## Publicação

Em **Settings → Pages**, deixe a origem como *Deploy from a branch*, branch
`main`, pasta `/ (root)`. Cada push para `main` republica o site em poucos
minutos.

## Desenvolvimento local

Basta abrir `index.html` no navegador. Se preferir servir por HTTP:

```sh
python -m http.server 8000
# http://localhost:8000
```

## Editando o conteúdo

Tudo está em `index.html`, em seções comentadas (`HERO`, `SERVIÇOS`,
`DIFERENCIAIS`, `EQUIPE`, `CONTATO / CTA`, rodapé). Cores, espaçamentos e raios
vêm de variáveis CSS declaradas em `:root`, no topo do `<style>`.

Telefones aparecem em dois lugares (cartões da equipe e bloco de contato) e usam
links `tel:` no formato internacional — ao alterar um número, atualize também o
`href`.
