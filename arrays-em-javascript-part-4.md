# Javascript Arrays - Part 4

![Pattern](https://images.unsplash.com/photo-1458682625221-3a45f8a844c7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80)

Nos primeiros artigos falamos um poucos sobre a criação e manipulação de arrays e esse é assunto bastante denso. Vale muito apena lermos e praticarmos muito além do que até agora foi apresentado.

Nesse artigo vamos fazer um apanhando dos principais métodos de arrays com exemplos. _So, let's get started_.

## Arrays methods

- _concat()_ - concatena arrays e retorna um novo array:

```js
const firstArray = [2, 5, 8];
const secondArray = [7, 5, 4];

const newArray = firstArray.concat(secondArray);

console.log(newArray); // [2, 5, 8, 7, 5, 4]
```

- _every()_ - recebe um função de callback que itera por cada elemento do array, usamos esse método para verifica se a condição passada no callback é atendida por todos os items do array.

```js
const firstArray = [2, 5, 8];

const hasOddNumberInArray = (number) => number % 2 !== 0;

console.log(firstArray.every(hasOddNumberInArray)); // false

const arrayWithOddNumbers = [1, 3, 5];

console.log(firstArray.every(hasOddNumberInArray)); // true
```

- _filter()_ - esse método retorna um novo array com o item ou items que retornam true para condição passada pelo função de callback recebida como parâmetro:

```js
const numbers = [1, 2, 5, 8];

const justEvenNumbers = numbers.filter((number) => number % 2 === 0);

console.log(justEvenNumbers); // [2,8]
```

- _forEach()_ - esse método executa uma função recebida como callback para cada item do array, mas não retorna nada e não afeta o array original:

```js
const numbers = [1, 2, 5, 8];
let total = 0;

numbers.forEach((number) => (total += number));

console.log(total); // 16
```

- _join()_ - esse método retorna os elementos do array agrupados em uma string separados por uma virgula, mas podemos passar um caractere separador:

```js
const date = [17, 10, 2021];

console.log(date.join()); // 17,10,2021
console.log(date.join("/")); // 17/10/2021
```

- _indexOf()_ - esse método retorna o índice do item passado por parâmetro ou -1 se não encontrado:

```js
const languages = ["Java", "JavaScript", "Python", "PHP", "GoLang"];

console.log(languages.indexOf("JavaScript")); // 1
console.log(languages.indexOf("C++")); // -1
```

- _reverse()_ - nesse método podemos inverter o array:

```js
const letters = ["A", "B", "C", "D", "E"];

console.log(letters.reverse()); // ['E', 'D', 'C', 'B', 'A']
```

- _sort()_ - esse método retorna o array ordenado alfabeticamente ou baseado em uma condição passada por callback:

```js
const numbers = [2, 8, 4, 3];

console.log(numbers.sort()); // [2, 3, 4, 8]

const users = [
  { name: "John", salary: 8000 },
  { name: "Matt", salary: 7850 },
  { name: "Steve", salary: 8100 },
];

console.table(users.sort((a, b) => a.salary - b.salary));
// return
[
  {
    name: "Matt",
    salary: 7850,
  },
  {
    name: "John",
    salary: 8000,
  },
  {
    name: "Steve",
    salary: 8100,
  },
];
```

- _toString()_ - devolve o array na forma de string:

```js
const names = ["John", "Steve", "Joe"];

console.log(names.toString()); // John,Steve,Joe
```

- _map()_ - retorna um novo array com os dados alterados por callback recebido:

```js
const numbers = [2, 4, 5, 1, 2];

const newArray = numbers.map((number) => number * 2);

console.log(newArray); // [4, 8, 10, 2, 4]
```

### End

Bem chegamos ao fim de mais um artigo sobre arrays, concerteza ainda existe muitos outros pontos a se explorar desse tema. Espero que tenha agregado algum conhecimento e aguarde os novos artigos em breve.

_See you next time_.

**_Thanks for your time..._**
