
# Popular JS Methods

:us: A brief explanation of the most popular 
JS methods and how to use them. Made this to 
personal study but decided to share the knowledge 
with the community

:brazil: Uma explicação rápido dos mais populares
métodos JS e como usá-los. Fiz isso com objetivo de estudo pessoal mas decidi
compartilhar o conhecimento com a comunidade

## filter()
:us: This function filters an array based on the
condition you provide and it returns a new array which contains 
items which satisfy those conditions

:brazil: Essa função filtra um array baseada na condição que você passa e retorna
um novo array que contém os itens que satisfazem as condições

```javascript
const temperatures = [10, 54, 15, 76, 24, 94];

const warmDays = temperatures.filter(dayTemperature => {
    return dayTemperature > 28;
})

console.log("Total warm days in week were: " + warmDays.length);
```

## map()
:us: Executes a loop over an array and convert each item to something you need

:brazil: Executa um loop em um array e converte cada um
dos itens para algo que você precisa

```javascript
const temperatureReadings = [10, 54, 15, 76, 24, 94];

const correctedTemperatureReadings = temperatureReadings.map(reading => reading + 10.5);

console.log(correctedTemperatureReadings);
```

## some()
:us: some() is very similar to filter(), but returns boolean instead.

:brazil: some() é muito similar ao filter(), mas retorna valor booleano no lugar.

```javascript
const animals = [
    {
        name: 'Dog',
        group: 'mammals'
    },
    {
        name: 'Eagle',
        group: 'birds'
    },
    {
        name: 'Snake',
        group: 'reptiles'
    },
];

const condition = 'birds';

// check if has birds
// checar se há pássaros

if (animals.some(animal => {
    return animal.group == condition
})) {
    console.log('Found some', condition)
}
```

## every()

:us: every() is also very similar to some() , but every() 
true only if every single element in array satisfy our condition.

:brazil: every() também é muito similar ao some(), mas every() apenas retorna true
se todos os elementos no array satisfazem a condição

```javascript
const isBelowAge = (currentAge) => currentAge < 40;

const firstArray = [1, 25, 39, 23, 34, 23, 12, 34];

console.log(firstArray.every(isBelowAge));
```

## shift()

:us: The shift() method removes the first element from an
array and returns without the removed element. This method changes the length of the array.

:brazil: O método shift() remove o primeiro elemento de um array
e retorna sem o elemento removido. Esse método muda o comprimento do array

```javascript
const foods = ['meat', 'chicken', 'milk', 'sugar', 'cheese', 'juice'];

foods.shift();

console.log(foods);
```

## unshift()
:us: Just like shift() method removes the first element from an array unshift() adds it.

:brazil: Assim como shift() remove o primeiro elemnto de um array, unshift() adiciona.

```javascript
const places = ['Paris', 'London', 'Manchester', 'Rio de Janeiro'];

places.unshift('Chapecó');

console.log(places)
```

## slice()

:us: The slice() method returns a shallow copy of 
a portion of an array into a new array object selected from
start to end (end not included) where start and end represent the 
index of items in that array. The original array will not be modified.

:brazil: O método slice() retorna uma cópia superficial de uma porção do array em um novo
array selecionado do início para o fim. Onde o início e fim represetam o index dos itens
daquele array. Nesse método não há a modificação do array original.

```javascript
let message = 'The quick brown fox jumps over the lazy dog';

let startIndex = message.indexOf('brown');

let endIndex = message.indexOf('jumps');

let newMessage = message.slice(startIndex, endIndex);

console.log(newMessage); 
```
## splice()

:us: splice() removes elements from an array using as first parameter the start index and in second the delete count

:brazil: splice() remove elementos de um array usando como primeiro parâmetro o index inicial e em segundo o número de itens que se quer remover

```javascript
const users = ['john', 'alfred', 'marcus', 'cecilia', 'alex'];

users.splice(2, 1);

console.log(users);
```