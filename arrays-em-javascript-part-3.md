# Javascript Arrays - Part 3

![Pattern](https://images.unsplash.com/photo-1458682625221-3a45f8a844c7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80)

Na primeira e na segunda parte do nosso estudo sobre arrays aprendemos as definições e como adicionarmos dados no início e no fim de um array. Vamos dá seguimento e aprenderemos mais alguns métodos para remoção de dados do array.

### Remove data in an array

Assim como foi para adicionarmos elementos no array tínhamos os métodos para adicionar no início ou no final do array, para removermos elementos temos a mesma lógica de métodos - método para remover no início do array e método para remover no final do array.

Para exemplificarmos teremos um lista de objetos com dados de grandes personalidades do mundo da tecnologia.

```js
const famousPerson = [
  { id: 1, name: "Steve Jobs", company: "Apple" },
  { id: 2, name: "Bill Gates", company: "Microsoft" },
  { id: 3, name: "Mark Zuckerberg", company: "Facebook/Meta" },
  { id: 4, name: "Elon Musk", company: "SpaceX" },
];
```

Agora vamos remover o Steve Jobs da nossa lista, e se observarmos ele esta no índice zero do nosso array, para isso usaremos o método _shift()_. Atenção para essa informação - o método _shift()_ retorna os dados removidos do array, no nosso caso, estará retornando o objeto no índice zero que tem as informações do Steve Jobs.

```js
const steveJobsInfo = famousPerson.shift();

console.log(steveJobsInfo)

//returns
{
    "id": 1,
    "name": "Steve Jobs",
    "company": "Apple"
}

console.log(famousPerson)

// returns
[
    {
        "id": 2,
        "name": "Bill Gates",
        "company": "Microsoft"
    },
    {
        "id": 3,
        "name": "Mark Zuckerberg",
        "company": "Facebook/Meta"
    },
    {
        "id": 4,
        "name": "Elon Musk",
        "company": "SpaceX"
    }
]
```

Agora nosso array que tinha quatro objetos tem somente três pois removemos o primeiro objeto. Só que agora eu quero remover o Elon Musk da lista, ou seja, o último elemento do nosso array, para isso usaremos o método _pop()_ que assim como o método usando anteriormente retorna os dados do objeto removido.

```js
const elonMuskInfo = famousPerson.pop();

console.log(elonMuskInfo)

//returns
{
    "id": 4,
    "name": "Elon Musk",
    "company": "SpaceX"
}

console.log(famousPerson)

// returns
[
    {
        "id": 2,
        "name": "Bill Gates",
        "company": "Microsoft"
    },
    {
        "id": 3,
        "name": "Mark Zuckerberg",
        "company": "Facebook/Meta"
    },

]
```

### Remove a specific item

Nosso array agora tem somente dois objetos. Certo, mas e se eu precisar remover do nosso array original, com quatro objetos, o Mark Zuckerberg, como eu faria?

Ao observamos o nosso array original veremos que o objeto com os dados do Mark está no índice dois - lembremos que a contagem dos índices de um array no javascript começa no zero.

Pois bem, vamos usar o método _splice()_. Esse método pode receber alguns parâmetros. O primeiro parâmetro que esse método recebe é o índice do objeto que será removido, como segundo parâmetro passamos quantos items queremos remover, no nosso caso apenas um item, por isso que a chamada do método fica assim: _famousPerson.splice(2,1)_. Esse método também retorna o objeto removido.

```js
const famousPerson = [
  { id: 1, name: "Steve Jobs", company: "Apple" },
  { id: 2, name: "Bill Gates", company: "Microsoft" },
  { id: 3, name: "Mark Zuckerberg", company: "Facebook/Meta" },
  { id: 4, name: "Elon Musk", company: "SpaceX" },
];

const markInfo = famousPerson.splice(2, 1);

console.log(markInfo);
// return
{
    "id": 3,
    "name": "Mark Zuckerberg",
    "company": "Facebook/Meta"
}

console.log(famousPerson);
// returns
[
    {
        "id": 1,
        "name": "Steve Jobs",
        "company": "Apple"
    },
    {
        "id": 2,
        "name": "Bill Gates",
        "company": "Microsoft"
    },
    {
        "id": 4,
        "name": "Elon Musk",
        "company": "SpaceX"
    }
]
```

### Bonus - add item with splice

Para finalizarmos o nosso artigo de hoje, vamos ver um uso muito legal do splice - com ele além de removermos um item específico do array ou vários, podemos também adicionar items ao array com o slice.

Temos um array de números e vamos adicionar um novo número no final do array, mas poderíamos adicionar em qualquer parte do array.

```js
const numbers = [1, 2, 3, 4];

numbers.splice(4, 1, 5);

console.log(numbers);

// return  [1, 2, 3, 4, 5]
```

### End of the Second part

O método _splice()_ tem vários usos além do mencionados, para aprender mais segue alguns links para leitura complementar.

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice

https://ricardo-reis.medium.com/splice-969723f47d26

Assim chegamos ao fim da terceira parte do nosso estudo de arrays em Javascript. Espero que tenha agregado algum conhecimento e _See you next time_.

**_Thanks for your time..._**
