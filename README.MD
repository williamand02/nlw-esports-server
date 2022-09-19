# NLW esports server

Projeto desenvolvido durante a nlw esports.

## Documentação da API

## Retorna todos os games

```
  GET /games
```

## Retorna anúncios por jogo

```
  GET /games/:id/ads
```

| Parâmetro | Descrição    |
| :-------- | :----------- |
| `:id`     | O ID do jogo |

## Cria um anúncio

```
  POST /games/:id/ads
```

| Parâmetro | Descrição                           |
| :-------- | :---------------------------------- |
| `:id`     | O ID do jogo que recebera o anúncio |
| body      | json                                |

Exemplo de json:

```js
{
  "name": "novo_nome",
  "yearsPlaying": 1,
  "discord": "nome de usuario discord",
  "weekDays": [0, 5, 6],
  "hourStart": "20:00",
  "hourEnd": "23:00",
  "useVoiceChannel": true
}
```

## Retorna discórdia por anúncio

```
  GET /ads/:id/discord
```

| Parâmetro | Descrição       |
| :-------- | :-------------- |
| `id`      | O ID do anúncio |

Rodar projeto

instale os pacotes:

```
npm install
```

gerar migrate

```
npx prisma migrate dev
```

\*_em ambiente de desenvolvimento_

## Stack utilizada

**Back-end:** Node, express, typescript, prisma, sqlite.
