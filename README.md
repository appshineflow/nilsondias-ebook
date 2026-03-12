# Guia do Investidor Global — Nilson Dias

Landing page de alta performance para o guia de investimentos internacionais.

## Antes do deploy — substitua os placeholders

No `index.html`, busque por:

1. `LINK_CHECKOUT_HOTMART` → substitua pelo link real do checkout (aparece 2x)
2. `assets/video/hero.mp4` → coloque o arquivo MP4 do vídeo na pasta `assets/video/`
3. `assets/images/nilson.jpg` → foto do Nilson em `assets/images/`
4. `assets/images/prova1.jpg`, `prova2.jpg`, `prova3.jpg` → frames do vídeo com prints de resultados
5. `assets/images/video-thumb.jpg` → thumbnail do vídeo (frame de capa)

## Deploy na Vercel

### 1. Criar repositório no GitHub
```bash
git init
git add .
git commit -m "feat: landing page guia investidor global"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/nilsondias-ebook.git
git push -u origin main
```

### 2. Conectar na Vercel
- Acesse vercel.com → New Project
- Importe o repositório do GitHub
- Framework Preset: **Other**
- Clique em Deploy

### 3. Adicionar domínio customizado
- Na Vercel: Settings → Domains → Add Domain
- Digite: `ebook.nilsondias.com`
- A Vercel vai mostrar o valor CNAME

### 4. Configurar DNS (Cloudflare)
- Type: `CNAME`
- Name: `ebook`
- Target: `cname.vercel-dns.com`
- Proxy: **OFF** (ícone cinza, não laranja)
- TTL: Auto

## Pixel Meta
ID já configurado: `641205538973535`
- PageView: dispara no load
- InitiateCheckout: dispara em todos os cliques no CTA

## Estrutura
```
nilsondias-ebook/
├── index.html
├── vercel.json
├── .gitignore
├── README.md
└── assets/
    ├── video/
    │   └── hero.mp4          ← adicionar manualmente
    └── images/
        ├── nilson.jpg        ← adicionar manualmente
        ├── video-thumb.jpg   ← adicionar manualmente
        ├── prova1.jpg        ← adicionar manualmente
        ├── prova2.jpg        ← adicionar manualmente
        └── prova3.jpg        ← adicionar manualmente
```
