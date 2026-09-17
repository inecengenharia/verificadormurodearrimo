# Muro de Arrimo — Verificação estrutural (INEC)

Aplicativo web para verificação de muro de arrimo (empuxos, tombamento,
deslizamento e tensões no solo), reproduzindo fielmente as fórmulas de uma
planilha de cálculo. Roda 100% no navegador, sem servidor.

## Publicar no GitHub Pages
1. Suba `index.html` e `app.js` na raiz do repositório.
2. Settings -> Pages -> Deploy from a branch -> branch `main`, pasta `/ (root)`.
3. Em ~1 min o app fica em `https://SEU-USUARIO.github.io/NOME-DO-REPO/`.

## Configurar antes de publicar
No arquivo `src/App.jsx`:
- `VIDEO_URL` — troque `"#"` pelo link do vídeo "como usar a planilha".
- `PONTES_URL` / `PROTENDIDO_URL` — links das pós (já preenchidos).

Depois de editar o `src/`, recompile:
```bash
npm i react react-dom esbuild
npx esbuild src/main.jsx --bundle --format=iife --loader:.jsx=jsx --minify --outfile=app.js
```

## Aviso
Ferramenta de apoio ao cálculo e conferência. Não substitui o projeto
estrutural nem as verificações normativas (ABNT NBR 6118, 6122, 11682). A
conferência de dados, hipóteses e resultados e a responsabilidade técnica
cabem ao engenheiro habilitado que a utiliza.
