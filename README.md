# Muro de Arrimo — Verificação estrutural

Aplicativo web para verificação de muro de arrimo (empuxos, tombamento,
deslizamento e tensões no solo), reproduzindo fielmente as fórmulas de uma
planilha de cálculo. Roda 100% no navegador, sem servidor.

## Como usar

Abra o link publicado (GitHub Pages) e edite os dados de entrada. Os
resultados e verificações são recalculados na hora.

## Publicando no GitHub Pages

1. Suba `index.html` e `app.js` na raiz do repositório.
2. Em **Settings → Pages**, selecione **Deploy from a branch**,
   branch `main` e pasta `/ (root)`. Salve.
3. Em ~1 minuto o app estará em `https://SEU-USUARIO.github.io/NOME-DO-REPO/`.

## Estrutura

- `index.html` — página que carrega o app
- `app.js` — aplicação compilada (React + lógica de cálculo, arquivo único)
- `src/` — código-fonte (App.jsx = componente; main.jsx = ponto de entrada)

## Recompilar (opcional)

Só é necessário se editar o `src/`.

```bash
npm i react react-dom esbuild
npx esbuild src/main.jsx --bundle --format=iife --loader:.jsx=jsx --minify --outfile=app.js
```

## Aviso

Ferramenta de apoio ao cálculo e conferência. Não substitui o projeto
estrutural nem as verificações normativas (ABNT NBR 6118, 6122, 11682). A
verificação de todos os dados, hipóteses e resultados, bem como a
responsabilidade técnica, cabem ao engenheiro habilitado que a utiliza.
