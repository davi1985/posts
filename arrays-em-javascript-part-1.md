# Javascript Arrays - Part 1

![Pattern](https://images.unsplash.com/photo-1458682625221-3a45f8a844c7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80)

Os arrays são uma estrutura de dados bastante comuns e amplamente utilizada no desenvolvimento de software. Nesse post aprenderemos um pouco sobre essa estrutura e seu comportamento na linguagem Javascript.

> Curiosidade: A primeira versão do Javascript não tinha suporte a arrays.

### What is it ?

Como já relatado no introdução, os arrays são uma estruturas de dados, e como estruturas eles possuem características predefinidas:

- Em algumas linguagens são usados para armazenar um mesmo tipo de dados, mas o Javascript permite que um array tenha diversos tipos de dados.
  ```js
  const myArray = ["john", 24, {}];
  // This array have string, number and object
  ```
- Geralmente a posição do primeiro dado inserido no array é a posição zero (0).
  ```js
  const myArray = ["john", "mari"];
  // The position where is the string 'jonh' is index 0.
  ```

## Simple Example

Provavelmente em algum momento do seu dia-a-dia como desenvolvedor talvez você precise armazenar os dias da semana. Sem utilizarmos os arrays podíamos ter uma solução como a do exemplo abaixo:

```js
const mon = "Monday";
const tue = "Tuesday";
const wed = "Wednesday";
const thu = "Thursday";
const fri = "Friday";
const sat = "Saturday";
const sun = "Sunday";
```

Observemos que criamos sete variáveis, uma para cada dia da semana, mas se utilizarmos os arrays podemos simplificar para uma única variável:

```js
const daysOfWeek = [
  "Monday",
  "Tuesday",
  "Wednesday",
  "Thursday",
  "Friday",
  "Saturday",
  "Sunday",
];
```

## Creating an array

Para criarmos um array em Javascript temos algumas opções:

- a partir do construtor que a linguagem disponibiliza:
  ```js
  const arrayByConstructor = new Array();
  ```
- podemos criar um array ja definindo a quantidade de elementos que ele terá:
  ```js
  const arrayByConstructorAndLength = new Array(5);
  // in this case the array has 5 elements with undefined value
  ```
- podemos criar já passando os valores no construtor:

```js
const arrayWithValuesInConstructor = new Array("John", "Mary", "Steve", "Paul");
```

Porém a forma mais comum de criarmos arrays em Javascript é com o uso de colchetes '[]':

```js
const myArrayEmpty = [];
const myArrayWithValues = ["John", "Mary", "Steve", "Paul"];
```

## Accessing an array element

Para acessarmos um elemento de dentro do array utilizamos o nome da variável assinalada ao array seguida de colchetes com o index desejado, lembrando que o primeiro elemento de um array está no index zero:

```js
const daysOfWeek = [
  "Monday",
  "Tuesday",
  "Wednesday",
  "Thursday",
  "Friday",
  "Saturday",
  "Sunday",
];

console.log(daysOfWeek[0]); // returns 'Monday'
console.log(daysOfWeek[1]); // returns 'Tuesday'
console.log(daysOfWeek[2]); // returns 'Wednesday'
console.log(daysOfWeek[3]); // returns 'Thursday'
console.log(daysOfWeek[4]); // returns 'Friday'
console.log(daysOfWeek[5]); // returns 'Saturday'
console.log(daysOfWeek[6]); // returns 'Sunday'
```

No exemplo acima acessamos cada elemento do array com o seu index específico, mas podemos usar uma estrutura de repetição como o `for of`:

```js
const daysOfWeek = [
  "Monday",
  "Tuesday",
  "Wednesday",
  "Thursday",
  "Friday",
  "Saturday",
  "Sunday",
];

for (day of daysOfWeek) {
  console.log(day);
}

// returns "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"
```

### End of the first part

Assim chegamos ao fim da primeira parte do nosso estudo de arrays em Javascript. Espero que tenha agregado algum conhecimento e _See you next time_.

**_Thanks for your time..._**
