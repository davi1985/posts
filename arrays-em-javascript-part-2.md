# Javascript Arrays - Part 2

![Pattern](https://images.unsplash.com/photo-1458682625221-3a45f8a844c7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80)

Na primeira parte dessa série de artigos vimos o que são arrays, como inicializá-los e como acessar os dados inseridos no array. Vamos dá seguimento falando agora sobre a manipulação dos dados.

> Curiosidade: Diferente daa linguagens Java e C - os arrays em Javascript são dinâmicos: pode-se adicionar e remover elementos facilmente.

### Add data in an array

Para adicionarmos novos elementos a um array, primeiro precisamos saber se queremos adicionaremos no início ou no final do array. Para exemplificar teremos um array com uma lista de objetos de _guitar heros_ onde em cada objeto temos dados referentes ao guitarrista e meu solo favorito:

```js
const guitarHeros = [
  { id: 1, name: "Steve Vai", bestSolo: "For the love of God" },
  { id: 2, name: "John Petrucci", bestSolo: "Another Day" },
  { id: 3, name: "Joe Satriani", bestSolo: "Friend" },
];
```

Então vamos adicionar mais um _guitar hero_, ninguém melhor que o nosso mestre brasileiro Kiko Loureiro, mas vamos adicionar **no fim do nosso array**, para isso usaremos o método _*push()*_ que a linguagem Javascript nos fornece.

```js
const kikoLoureiro = { id: 4, name: "Kiko Loureiro", bestSolo: "Nova Era" };

guitarHeros.push(kikoLoureiro);
```

Se dermos um _console.log()_ para visualizarmos o nosso array teremos o seguinte resultado:

```js
console.log(guitarHeros);

[
  {
    id: 1,
    name: "Steve Vai",
    bestSolo: "For the love of God",
  },
  {
    id: 2,
    name: "John Petrucci",
    bestSolo: "Another Day",
  },
  {
    id: 3,
    name: "Joe Satriani",
    bestSolo: "Top Gun",
  },
  {
    id: 4,
    name: "kiko Loureiro",
    bestSolo: "Nova Era",
  },
];
```

Observemos que os dados do Kiko estão inserido no final do nosso array. Uma curiosidade sobre o método _push()_ é que ele retorna o tamanho do array, mais um simples exemplo para entendermos:

```js
const numbers = [2, 3, 5, 1, 4];

const addNewNumberIntoArrayNumbers = numbers.push(12);

console.log(addNewNumberIntoArrayNumbers); // return 6 - this is array length
```

No exemplo acima temos um array de números, criamos então uma variável _addNewNumberIntoArrayNumbers_ para pegarmos o retorno do método _push()_ onde estamos adicionando o número 12 a nosso array, por fim damos um _console.log()_ na nossa variável _addNewNumberIntoArrayNumbers_ e vemos que o retorno é 6 que é exatamente o tamanho do nosso array.

## I'm almost done!

Para finalizar esse artigo vamos conhecer mais um método de manipulação de arrays, vamos aprender a adicionar elementos no início do array. No exemplo abaixo temos novamente uma lista objetos com dados de algumas linguagens, mas especificamente nome e ano de criação da linguagem.

```js
const languages = [
  { id: 1, name: "Python", birth: 1989 },
  { id: 2, name: "PHP", birth: 1994 },
  { id: 3, name: "Javascript", birth: 1995 },
];
```

Vamos adicionar a nossa lista de linguagens as informações referentes a linguagem C++, mas vamos adiciona no início do nosso array, para isso usaremos o método _unshift()_:

```js
const cPlusPlus = { id: 4, name: "C++", birth: 1983 };

languages.unshift(cPlusPlus);
```

Se dermos um _console.log()_ para visualizarmos o nosso array agora teremos o seguinte resultado:

```js
console.log(languages);

[
  {
    id: 4,
    name: "C++",
    birth: 1983,
  },
  {
    id: 1,
    name: "Python",
    birth: 1989,
  },
  {
    id: 2,
    name: "PHP",
    birth: 1994,
  },
  {
    id: 3,
    name: "Javascript",
    birth: 1995,
  },
];
```

Observe que os dados referente a linguagem C++ estão no início do nosso array. É importante também saber que o método _unshift()_ também retorna o tamanho do array atualizado.

### End of the Second part

Assim chegamos ao fim da segunda parte do nosso estudo de arrays em Javascript. Espero que tenha agregado algum conhecimento e _See you next time_.

**_Thanks for your time..._**
