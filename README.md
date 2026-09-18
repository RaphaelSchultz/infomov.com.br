# Site Infomov — Parceiro Bitrix24

Site institucional da **Infomov**, parceira **Silver Bitrix24**: licenciamento,
implementação, consultoria e suporte do Bitrix24, com os planos e preços oficiais.

Site estático de arquivo único (`index.html`) — sem build, sem dependências.

## Estrutura

```
index.html   → o site (HTML + CSS + JS embutidos; logo em data URI)
logo.png     → logo da Infomov (favicon / og:image)
.nojekyll    → faz o GitHub Pages servir os arquivos como estão
```

## Publicar no GitHub Pages

1. Suba estes arquivos para o seu repositório (veja os comandos abaixo).
2. No repositório: **Settings → Pages**.
3. Em **Source**, escolha a branch `main` e a pasta `/root`. Salve.
4. Em ~1 min o site fica no ar em `https://SEU-USUARIO.github.io/SEU-REPO/`
   (ou no seu domínio, se configurar um `CNAME`).

### Subir pela primeira vez

```bash
git init
git add .
git commit -m "Site Infomov - parceiro Bitrix24"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/SEU-REPO.git
git push -u origin main
```

### Atualizar depois

```bash
git add .
git commit -m "Atualiza site"
git push
```

## Atualizar os planos / preços

Todos os valores ficam em **um único array `DATA`** dentro do `index.html`
(procure por `var DATA`). Cada plano tem só dois números-base:

- `mensal` → mensalidade cheia (cobrança mensal)
- `am`     → mensalidade na cobrança anual (já com desconto)

O site calcula sozinho: **trimestral = 3× `mensal`**, **anual = 12× `am`**,
e o percentual de economia. É só trocar esses números quando o Bitrix24 reajustar.

> Planos, valores e recursos conforme o site oficial do Bitrix24
> (https://www.bitrix24.com.br/prices/), consultados em setembro de 2026.
> Bitrix24 é marca de seus respectivos titulares.

## Contato

- WhatsApp: (27) 99720-5870
- E-mail: contato@infomov.com.br
