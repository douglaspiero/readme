# ECMAScript### - Exemplos

### Nullish Coalescing Operator

```javascript
const idade = null;
document.body.innerText = 'Sua idade é: ' + (idade ?? 'Não informado')
```

### Objetos

```javascript

const user = {
  name : 'Douglas',
  idade : 34,
  address : {
    street : 'Rua Tals',
    number : 176,
  },
};


// Retorna as keys do Objeto

document.body.innerText = Object.keys(user)

// Retorna todos os valores do Objeto

document.body.innerText = JSON.stringify(Object.values(user))

// Retorna um vetor com subvetores

document.body.innerText = JSON.stringify(Object.entries(user))

```

### Desestruturação

```javascript
const address = user.address

const {address, idade} = user

document.body.innerText = JSON.stringify({address, idade})

const {address, idade : age} = user > Renomear key

const {address, idade : age, nickname = 'Piero'} = user // Adicionar valor padrão a uma nova key

document.body.innerText = JSON.stringify({address, age, nickname})

// Função com Desestruturação

function mostraIdade({idade}) {
  return idade
}
document.body.innerText = mostraIdade(user)
```

// Rest operator

/*
const {name, idade, ...rest} = user

document.body.innerText = JSON.stringify(rest)
*/
/*
const array = [1, 2, 3, 4, 5, 6, 7, 8, 9]

const [first, second, ...rest] = array

document.body.innerText = JSON.stringify({first, second, rest})
*/

// Optinal Chaining

/*
const user = {
  name : 'Douglas',
  age : 34,
  address : {
    street : 'Rua Tals',
    number : 176,
      zip: {
        code : '15352000',
        city : 'São Paulo'
      },
      showFullAddress() {
        return 'ok'
      }
  },
};

document.body.innerText = user.address?.zip?.code ?? 'Não Informado'

*/

//Metodos de array

//const array = [1, 2, 3, 4, 5, 6, 7, 8, 9]

//For
// for (const i of array) {
//   document.body.innerText += " " + i 
// }

//ForEach
// array.forEach(item => {
//   document.body.innerText += " " + item 
// })

// map, filter, every, some, find, findIndex, reduce


//map

// const newArray = array.map(item => {
//   return item * 2
// })
// document.body.innerText = JSON.stringify(newArray)

// const newArray = array.map(item => {
//   if (item % 2 == 0) {
//     return item * 10
//   }
//     return item
// })
// document.body.innerText = JSON.stringify(newArray)

//filter
// const newArray = array
//   .filter(item => item % 2 === 0)
//   .map(item => item * 10)
//document.body.innerText = JSON.stringify(newArray)

//every
// const todosItensSaoNumeros = array.every(item => typeof item === 'number')
// document.body.innerText = JSON.stringify(todosItensSaoNumeros)

//sone
// const peloMenosUmItemNaoEUmNumero = array.some(item => {
//   return typeof item != 'number'
// })

//find
// const par = array.find(item => item % 2 === 0)
// document.body.innerText = JSON.stringify(par)

//findIndex
// const par = array.findIndex(item => item % 2 === 0)
// document.body.innerText = JSON.stringify(par)

//reduce
// const soma = array.reduce((acc, item) => {
//   document.body.innerText += acc + ' , ' + item 
//   return acc + item
// }, 0)
// document.body.innerText = JSON.stringify(soma)

//Templete Literals

// const name = "Douglas"
// const message = `Bem-vindo, ${name}`
// document.body.innerText = JSON.stringify(message)

//Promises > .then / .catch

// fetch('https://api.github.com/users/douglaspiero')
//   .then(response => {
//     response.json().then(body => {
//       console.log(body)
//     })
//   })
//   .catch(err => {
//     console.log(err)
// })

// async function buscaDadosNoGithub() {
//   try {
//     const response = await fetch('https://api.github.com/users/douglaspiero')
//     const body = await response.json()
//     console.log(body.name) 
//   } catch (error) {
//     console.log(error)
//   } finally {
//     console.log('deu')
//   }
// }

// buscaDadosNoGithub().then(name => {
//   console.log(name)
// })





