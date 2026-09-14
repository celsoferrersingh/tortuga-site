# Publicar o site do Tortuga no GitHub Pages

O site é **um único arquivo** (`index.html`), sem dependências externas — não precisa
compilar nada. Escolha uma das opções abaixo.

## Opção A — Repositório dedicado (URL mais limpa) — recomendado
1. No GitHub, crie um repositório novo, ex.: **tortuga-site** (público).
2. Suba o arquivo `index.html` para a raiz desse repositório:
   ```powershell
   cd C:\tortuga\site
   git init
   git add index.html
   git commit -m "Site do Tortuga"
   git branch -M main
   git remote add origin https://github.com/SEU_USUARIO/tortuga-site.git
   git push -u origin main
   ```
3. No repositório: **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   Branch: **main** / **/ (root)** → Save.
4. Em ~1 minuto o site fica no ar em:
   `https://SEU_USUARIO.github.io/tortuga-site/`

## Opção B — Dentro do repositório atual (pasta /docs)
1. Copie `index.html` para uma pasta `docs/` na raiz do projeto `tortuga`.
2. Commit e push (junto do resto do projeto).
3. **Settings → Pages → Source: Deploy from a branch**, Branch: **main** / **/docs** → Save.
4. URL: `https://SEU_USUARIO.github.io/tortuga/`

## Opção C — Site pessoal (raiz do seu usuário)
Se criar um repositório chamado **SEU_USUARIO.github.io** e colocar o `index.html` na raiz,
o site fica em `https://SEU_USUARIO.github.io/` (sem sufixo).

---
Dica: depois de publicar, teste o link no celular também — o site é responsivo.
Para atualizar, basta editar o `index.html`, dar `git commit` e `git push`.
