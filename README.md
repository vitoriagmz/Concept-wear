# Concept Wear

Site institucional para a Concept Wear — loja de roupas masculinas e perfumes importados. Identidade visual em preto e dourado, 4 páginas estáticas (HTML/CSS/JS puro, sem dependências de build).

## Estrutura

```
index.html       # Home
produtos.html     # Catálogo com filtro por categoria
sobre.html        # História e valores da marca
contato.html       # Contato + formulário (visual, sem backend)
styles.css        # Todo o design system (cores, tipografia, layout)
README.md
```

Todos os arquivos ficam soltos na mesma pasta (sem subpastas) — baixe todos e coloque-os juntos no mesmo diretório antes de abrir `index.html` ou subir para o GitHub.

Todas as imagens de produto são placeholders desenhados em SVG (contornos dourados). Basta trocar o bloco `<div class="product-media">` de cada produto por uma tag `<img>` apontando para a foto real quando você tiver o material fotográfico.

## Rodar localmente

Não precisa de servidor nem de instalação — é só abrir `index.html` no navegador. Se preferir um servidor local simples (recomendado para o menu funcionar 100% igual ao ambiente final):

```bash
cd concept-wear
python3 -m http.server 8000
# depois acesse http://localhost:8000
```

## Como criar o repositório no GitHub

Baixe esta pasta, extraia e siga os passos abaixo no terminal, dentro da pasta `concept-wear`.

### 1. Crie o repositório no site do GitHub
1. Acesse [github.com/new](https://github.com/new)
2. Nome do repositório: `concept-wear` (ou o nome que preferir)
3. Deixe **"Add a README"**, `.gitignore` e licença **desmarcados** (você já tem um README aqui)
4. Clique em **Create repository**
5. Copie a URL que o GitHub mostrar, algo como `https://github.com/SEU-USUARIO/concept-wear.git`

### 2. Suba o projeto local
```bash
cd concept-wear
git init
git add .
git commit -m "Primeira versão do site Concept Wear"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/concept-wear.git
git push -u origin main
```

Se preferir usar o GitHub CLI (`gh`) em vez do site, os passos 1 e 2 viram só:
```bash
cd concept-wear
git init && git add . && git commit -m "Primeira versão do site Concept Wear"
gh repo create concept-wear --public --source=. --push
```

### 3. (Opcional) Publicar o site com GitHub Pages
1. No repositório, vá em **Settings → Pages**
2. Em **Source**, selecione a branch `main` e a pasta `/ (root)`
3. Salve — em alguns minutos o site fica disponível em `https://SEU-USUARIO.github.io/concept-wear/`

## Próximos passos sugeridos
- Trocar os SVGs placeholder pelas fotos reais dos produtos e o logo definitivo.
- Conectar o formulário de contato a um serviço como Formspree, EmailJS ou um backend próprio (hoje ele só mostra um alerta de exemplo).
- Ajustar preços, endereço, WhatsApp e Instagram para os dados reais da loja.
