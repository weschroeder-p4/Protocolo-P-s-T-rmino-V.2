# Protocolo Pós Término — Página de Vendas (Low Ticket)

Página estática (HTML/CSS) para publicação no **GitHub Pages** com domínio
`ppt.joaochesca.com.br`.

## Estrutura
```
/
├── index.html              → a página
├── CNAME                   → domínio (ppt.joaochesca.com.br) — não apagar
├── .nojekyll               → impede o GitHub de processar com Jekyll
├── README.md
└── assets/
    ├── css/brand.css       → design system (paleta + tipografia da marca)
    └── img/                → imagens da página (hero, ícone, mockups)
```

## Como publicar no GitHub Pages
1. Crie um repositório (ex.: `protocolo-pos-termino`) e suba **todos** estes arquivos na raiz.
2. Em **Settings → Pages**, em *Build and deployment*, escolha *Deploy from a branch* →
   branch `main` / pasta `/ (root)`.
3. Aguarde o deploy. O arquivo `CNAME` já define o domínio personalizado.

## Cloudflare → GitHub Pages
No DNS da Cloudflare, crie um registro **CNAME**:
- **Name:** `ppt`
- **Target:** `<seu-usuario>.github.io`
- **Proxy:** pode deixar "DNS only" (nuvem cinza) até o certificado do GitHub emitir; depois pode ligar o proxy.

O GitHub emite o certificado HTTPS automaticamente para o domínio do `CNAME`.

## Tipografia
Fontes carregadas do Google Fonts: **DM Serif Display** (títulos) e **Manrope** (textos).

## Antes de publicar — 2 ajustes finais
1. **Link do checkout:** no fim do `index.html`, no `<script>`, troque
   `var CHECKOUT_URL = "#";` pela URL do seu checkout (Hotmart/Kiwify/etc.).
   Todos os botões de compra passam a apontar para lá automaticamente.
2. **Foto do João Chesca (Bloco 11 – Autoridade):** coloque a foto em
   `assets/img/joao-chesca.jpg` e, no bloco `#foto-joao`, troque o placeholder
   pela linha comentada: `<img src="assets/img/joao-chesca.jpg" alt="Psicólogo João Chesca" />`.

Opcional: criar as páginas `termos.html` e `privacidade.html` (os links do rodapé já apontam para elas).

## Conteúdo
Página construída a partir da copy oficial (14 blocos). O bloco de **Depoimentos**
foi omitido a pedido — quando houver provas reais, é só reativar.
