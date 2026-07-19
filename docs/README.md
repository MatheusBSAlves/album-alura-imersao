# Álbum Alura - Frontend para GitHub Pages

Este diretório contém os arquivos que podem ser utilizados para publicar o frontend estático no GitHub Pages.

Coloque os seguintes arquivos em `docs/`:

- `index.html`
- `style.css`
- `app.js`
- `figurinhas/` (pasta de imagens)

O backend Python não é suportado pelo GitHub Pages. Para consumir a API a partir do frontend hospedado em Pages, use o parâmetro `?api=` na URL.

Exemplo:

`https://<seu-usuario>.github.io/<seu-repo>/?api=https://meu-backend.herokuapp.com`
