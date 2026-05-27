# Home 360 — Site Institucional

Site moderno, leve e otimizado para SEO. Tudo em um único `index.html` para facilitar edições.

---

## 📁 Estrutura de arquivos

```
h360/
├── index.html         ← o site
├── instagram-links.txt ← links dos posts do Instagram (edite aqui)
├── sitemap.xml        ← mapa do site (SEO)
├── robots.txt         ← instruções para Google
├── README.md          ← este arquivo
└── imagens/           ← TODAS as imagens vão aqui dentro
    ├── logo-home360.png
    ├── fundo_hero.jpg
    ├── quem-somos.jpg
    ├── audio-video.jpg
    ├── casa-inteligente.jpg
    ├── corporativo.jpg
    ├── instagram-1.jpg   (a maior, em destaque no mosaico)
    ├── instagram-2.jpg
    ├── instagram-3.jpg
    ├── instagram-4.jpg
    ├── instagram-5.jpg
    └── instagram-6.jpg
```

**⚠️ Importante:** o `index.html` precisa estar na MESMA pasta que a subpasta `imagens/`. Não deixe os arquivos soltos.

---

## 🖼️ Como trocar qualquer imagem

Cada imagem do site tem um **nome fixo padrão**. Para trocar, é só substituir o arquivo na pasta `imagens/` pelo novo, mantendo o mesmo nome. **Não precisa mexer no HTML.**

| O que você vê no site | Nome do arquivo |
|---|---|
| Fundo do Hero (banner principal) | `imagens/fundo_hero.jpg` |
| Foto da seção "Quem somos" | `imagens/quem-somos.jpg` |
| Card "Áudio e Vídeo" | `imagens/audio-video.jpg` |
| Card "Casa Inteligente" | `imagens/casa-inteligente.jpg` |
| Card "Corporativo" | `imagens/corporativo.jpg` |
| Portfólio — foto grande do mosaico | `imagens/instagram-1.jpg` |
| Portfólio — fotos menores | `imagens/instagram-2.jpg` até `instagram-6.jpg` |

### Aceita `.jpg` ou `.png`

O sistema tenta primeiro o arquivo `.jpg`. Se não achar, tenta `.png`. Então tanto faz qual formato você usar — desde que o nome esteja correto.

**Recomendação:** prefira **JPG** para fotos (arquivo menor, carrega mais rápido). PNG só vale a pena se a imagem tem transparência ou texto/gráficos com bordas duras.

### Dimensões sugeridas

| Imagem | Largura ideal |
|---|---|
| Hero (fundo do banner) | 2000–2500px (foto larga) |
| Quem somos | 900–1200px |
| Cards de soluções | 1200–1600px |
| Instagram-1 (grande) | 900px quadrada |
| Instagram-2 a 6 (pequenas) | 400–600px quadradas |

Não precisa ser exato — o navegador redimensiona. Mas evite imagens muito pequenas (vai ficar pixelada) ou gigantes (vai demorar pra carregar).

---

## 🚀 Como colocar no ar

**Pelo GitHub Pages** (recomendado, grátis):

1. Crie um repositório no GitHub
2. Suba a pasta `h360/` inteira (com a subpasta `imagens/`)
3. Em **Settings → Pages**, escolha "Deploy from a branch", branch `main`, pasta `/(root)`
4. Em alguns minutos, seu site fica online em `https://seu-usuario.github.io/nome-do-repo`
5. Para usar `h360.com.br`, adicione em "Custom domain" e configure o DNS

Outras opções de hospedagem grátis: **Netlify**, **Vercel**, **Cloudflare Pages**.

---

## 💬 Mensagem do WhatsApp

Todos os botões de WhatsApp abrem a conversa com uma mensagem pré-pronta. Para editar essa mensagem ou o número:

Abra o `index.html`, busque por `WA_NUMERO` (Ctrl+F). Você vai encontrar:
```js
const WA_NUMERO = '5585987614427';
const WA_MENSAGEM = 'Olá Home 360! Vi o site de vocês e gostaria de saber mais sobre as soluções em automação, áudio e vídeo.';
```

Edite essas duas linhas. Tudo se atualiza sozinho em todos os botões.

---

## ✏️ Edições rápidas

### Textos do site
Abra o `index.html` num editor (recomendo **VS Code**, gratuito). Use **Ctrl+F** para buscar o trecho a editar.

### Telefone e e-mail
Ctrl+F e troque diretamente:
- `(85) 98761-4427`
- `home@h360.com.br`
- `5585987614427` (formato dos links)

### Cores
Procure por `:root {` no início do CSS. Mude o valor de qualquer variável:
```css
--accent: #c9a96e;       /* Dourado champanhe — cor principal */
--bg-deep: #0a0a0a;      /* Preto de fundo */
--text-primary: #f5f1ea; /* Cor do texto */
```

### Estatísticas do "Sobre" (10+ anos, 200+ projetos)
Procure por `stat-number`. Troque os números.

---

## 📧 Formulário de contato

Hoje o formulário abre o WhatsApp com a mensagem montada. Para receber também por e-mail:

### Formspree (tem plano grátis)
1. Conta em `formspree.io`
2. Pegue o link `https://formspree.io/f/seuCodigo`
3. No HTML, troque a tag `<form>` para:
   ```html
   <form class="contact-form reveal" action="https://formspree.io/f/seuCodigo" method="POST">
   ```
4. Remova o `onsubmit="return enviarFormulario(event)"`

---

## 🔍 SEO

Já configurado: title, meta description, Open Graph (preview no WhatsApp/Facebook), Schema.org LocalBusiness, sitemap.xml, robots.txt, HTML semântico.

**Próximos passos depois de publicar:**
1. **Google Search Console** — cadastre o site e envie o `sitemap.xml`. Mais importante para aparecer no Google.
2. **Google Meu Negócio** — turbina o SEO local em Fortaleza.

---

## 📸 Sobre o Portfólio / Instagram

Hoje as 6 fotos do mosaico são manuais. Para atualizar, é só trocar os arquivos `instagram-1.jpg` a `instagram-6.jpg` na pasta `imagens/`.

A `instagram-1.jpg` é a maior (em destaque). As outras são as menores ao redor.

### Linkar cada foto para o post específico no Instagram

No arquivo `instagram-links.txt` (na raiz da pasta) você pode colar o link de cada post correspondente. Formato:

```
instagram-1 - https://www.instagram.com/p/CODIGO_DO_POST/
instagram-2 - https://www.instagram.com/p/OUTRO_CODIGO/
...
```

Aceita `-`, `:` ou `=` como separador. Linhas começadas com `#` são comentários. Se uma entrada ficar vazia, a foto correspondente abre o perfil em vez do post.

**⚠️ Atenção:** o navegador só consegue ler esse arquivo quando o site está **no ar** (GitHub Pages, Netlify etc.) por causa de uma trava de segurança do Chrome com arquivos locais. Se você abrir o `index.html` direto no Chrome para preview, os links continuam funcionando — só vão pro perfil em vez do post específico. **Quando publicar no servidor, os links dos posts entram em ação automaticamente.**

### Integração automática com Instagram no futuro

Se quiser que as fotos do mosaico atualizem sozinhas conforme você posta:
- **Behold.so**, **Elfsight**, **LightWidget** — widgets de terceiros (têm plano grátis e pago, verifique antes)
- **GitHub Actions com API do Instagram** — mais técnico, requer tokens que expiram a cada 60 dias

Para um site institucional, manual costuma ser melhor — você escolhe quais posts entram.

---

Qualquer ajuste, é só pedir.
