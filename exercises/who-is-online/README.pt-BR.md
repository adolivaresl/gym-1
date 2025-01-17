---
difficulty:
  - Beginner
OAs:
  - Objetos (key, value)
projects:
  - Data-lovers
---

# Who's online?

Você tem um aplicativo de bate-papo, como você sabe quem está online?

Você quer mostrar a seus usuários quais de seus amigos estão online e
disponível para conversar.

Dada uma matriz de objetos contendo nome de usuário, status e tempo desde
a última atividade (em minutos), crie uma função para determinar quem é
`online`, `offline` y `away`.

Se alguém está `online` mas sua `lastActivity` foi há mais de 10 minutos, então
é considerado `away`.

Os dados de entrada têm a seguinte estrutura:

```js
[
  {
    username: "David",
    status: "online",
    lastActivity: 10,
  },
  {
    username: "Lucy",
    status: "offline",
    lastActivity: 22,
  },
  {
    username: "Bob",
    status: "online",
    lastActivity: 104,
  },
];
```

A saída correspondente aos dados de entrada seria a seguinte:

```js
{
  online: ['David'],
  offline: ['Lucy'],
  away: ['Bob']
}
```

Se, por exemplo, nenhum usuário estiver online, a saída deverá ficar assim:

```js
{
  offline: ['Lucy'],
  away: ['Bob']
}
```

`username` sempre será uma string; `status` sempre será um dos seguintes
valores: `online` o `offline`; `lastActivity` sempre será um número >= 0.

Por fim, se você não tiver amigos em seu aplicativo de bate-papo, a entrada será
uma matriz vazia `[]`. Se for esse o caso, você deve retornar um objeto `{}` vazio.
