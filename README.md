# Álbum Alura - Imersão

Projeto de exemplo para um álbum de figurinhas com frontend e backend.

## Objetivo

Criar uma API em Python usando FastAPI para servir figurinhas e imagens, além de um frontend estático que exibe o álbum.

## Funcionalidades

- `main.py`: servidor FastAPI com:
  - endpoint `GET /` retornando `{"mensagem": "Olá, mundo! 🌍"}`
  - endpoint `GET /figurinhas` que retorna a lista de figurinhas
  - endpoint `GET /figurinhas/{id}/imagem` que retorna a imagem da figurinha
  - configuração CORS para aceitar qualquer origem
  - montagem de arquivos estáticos em `/imgs`

- `index.html`: frontend estático do álbum com navegação e visualização de páginas.
- `style.css`: estilos do frontend, incluindo o esquema de cores no bloco `:root`.
- `app.js`: lógica do álbum, animações, controles e interações do usuário.
- `figurinhas/`: pasta com as imagens das figurinhas.
- `prompts/`: arquivos de exercícios e instruções usadas para evoluir o projeto.

## GitHub Pages

O backend em Python (`main.py`) não pode ser implantado diretamente no GitHub Pages, porque Pages serve apenas sites estáticos. Para usar o frontend hospedado em Pages com o backend do projeto:

- Configure o GitHub Pages para publicar a pasta `docs/`.
- Use um backend Python externo ou um serviço separado que execute `main.py`.
- A URL do frontend deve incluir `?api=` apontando para esse backend.

Exemplo:
`https://<seu-usuario>.github.io/<seu-repo>/?api=https://meu-backend.herokuapp.com`

> No projeto raiz, o frontend ainda usa `http://localhost:8000` por padrão, então localmente você pode rodar o backend e abrir `index.html` para ver tudo funcionando.

## Vercel

Se você fizer deploy no Vercel, use o frontend estático em `docs/` e passe a URL do backend como query string:

`https://<seu-projeto>.vercel.app/?api=https://meu-backend.herokuapp.com`

O backend FastAPI não roda diretamente no Vercel sem conversão para funções serverless, portanto a forma mais segura é hospedar o backend em outro serviço e apontar o frontend para ele.

## Notas

- As cores do projeto são definidas em `style.css` dentro do bloco `:root`.
- A pasta `figurinhas/` contém os arquivos de imagem usados pela API e pelo frontend.
