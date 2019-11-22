## JavaScript let

A instrução `let` permite declarar uma variável com escopo de bloco.

##### Example
```js
var x = 10;
// Here x is 10
{
 let x = 2;
 // Here x is 2
}
// Here x is 10
```

## JavaScript const

A instrução `const` permite declarar uma constante (uma variável JavaScript com um valor constante).
As constantes são semelhantes a deixar variáveis, exceto que o valor não pode ser alterado.

##### Example

```js
var x = 10;
// Here x is 10
{
 const x = 2;
 // Here x is 2
}
// Here x is 10
```

## Classes no ES6

<p align="justify">
Uma classe é um tipo de função, mas, em vez de usar a palavra function - chave para iniciá-la, usamos a palavra-chave classe as propriedades são atribuídas dentro de um constructor() método.
</p>
<p align="justify">
Use a palavra class- chave para criar uma classe e sempre adicione um método construtor.<br />
O método construtor é chamado sempre que o objeto de classe é inicializado.
</p>

##### Exemplo
Uma definição de classe simples para uma classe chamada "Pessoa":

```JS
class Pessoa {
  constructor(nome) {
    this.Nome = nome;
  }
}
```
<p align="justify">
Criando objetos usando a classe Pessoa:
</p>

```JS
class Pessoa {
  constructor(nome) {
    this.Nome = nome;
  }
}
pessoa = new Pessoa("Nome da Pessoa");
```

## Valores de parâmetro padrão
ES6 permite que os parâmetros de função tenham valores padrão.

```JS
function fn(x, y = 5) {
  // y é 5 se nenhum valor for passado como parametro
  return x + y;
}
fn(5); // retorna 10
```

## Array Find

<p align="justify">
O find() método retorna o valor do primeiro elemento da matriz que passa em uma função de teste.
Este exemplo localiza (retorna o valor de) o primeiro elemento maior que 18:
</p>

##### Exemplo

```JS
var numbers = [4, 9, 16, 25, 29];
var first = numbers.find(myFunction);

function myFunction(value, index, array) {
  return value > 18;
}
```
Observe que a função usa 3 argumentos:

- O valor do item
- O índice do item
- A própria matriz


## Array FindIndex

O findIndex()método retorna o índice do primeiro elemento da matriz que passa em uma função de teste.
Este exemplo localiza o índice do primeiro elemento maior que 18:

##### Exemplo
```JS
var numbers = [4, 9, 16, 25, 29];
var first = numbers.findIndex(myFunction);

function myFunction(value, index, array) {
  return value > 18;
}
```
Observe que a função usa 3 argumentos:

- O valor do item
- O índice do item
- A própria matriz


## Novas Propriedades de Número
O ES6 adicionou as seguintes propriedades ao objeto Number:

- EPSILON
- MIN_SAFE_INTEGER
- MAX_SAFE_INTEGER

##### Exemplo
```js
var x = Number.EPSILON;
var x = Number.MIN_SAFE_INTEGER;
var x = Number.MAX_SAFE_INTEGER;
```
## Novos Métodos Numéricos
O ES6 adicionou 2 novos métodos ao objeto Number:

- Number.isInteger()
- Number.isSafeInteger()

#### O método Number IsInteger
O Number.isInteger() método retornará truese o argumento for um número inteiro.

##### Exemplo
```js
Number.isInteger(10);        // returns true
Number.isInteger(10.5);      // returns false
```
#### O método Number IsSafeInteger
Um número inteiro seguro é um número inteiro que pode ser representado exatamente como um número de precisão dupla.
O Number.isSafeInteger() método retornará truese o argumento for um número inteiro seguro.

##### Exemplo
```js
Number.isSafeInteger(10);    // returns true
Number.isSafeInteger(12345678901234567890);  // returns false
```

> *Inteiros seguros são todos os números inteiros de - (2 53 - 1) a + (2 53 - 1).*
>
> *Isso é seguro: 9007199254740991.*
>
> *Isso não é seguro: 9007199254740992.*

## Novos Métodos Globais
O ES6 também adicionou 2 novos métodos de número global:

- isFinite()
- isNaN()

#### O Método IsFinite

O isFinite()método global retornará falsese o argumento for Infinityou NaN.

Caso contrário, ele retorna true:

##### Exemplo

```js
isFinite(10/0);       // returns false
isFinite(10/1);       // returns true
```

#### O Método IsNaN 

O mundial `isNaN()`método retorna `true`se o argumento for `NaN`. Caso contrário, ele retorna `false`:

##### Exemplo

```js
isNaN("Hello");    // returns true
```

## Operador de Exponenciação

O operador de **exponenciação** ( `**`) eleva o primeiro operando à potência do segundo operando.

##### Exemplo
```js
var x = 5;
var z = x ** 2;     // result is 25
```

> `x ** y` produz o mesmo resultado que `Math.pow(x,y)`:

##### Exemplo
```js
var x = 5;
var z = Math.pow(x,2);  // result is 25
```

## Higher-Order Functions

#### Função de Ordem Superior

<p align="justify">
Em matemática e ciências da computação, uma função de ordem superior é uma função que executa pelo menos um dos seguintes procedimentos: assume uma ou mais funções como argumentos (ou seja, parâmetros processuais), retorna uma função como resultado.
Todas as outras funções são de primeira ordem. Em matemática, funções de ordem superior também são denominadas operadores ou funcionais. O operador diferencial no cálculo é um exemplo comum, pois mapeia uma função para sua derivada, também uma função. Funções de ordem superior não devem ser confundidas com outros usos da palavra "functor" ao longo da matemática.
</p>

> <p align="justify">	
> 	<b>Functor: </b> <i>(em teoria das categorias, é um mapeamento entre categorias que preserva estruturas).</i>
> </p>
>

<p align="justify">
No cálculo lambda sem tipo, todas as funções são de ordem superior; em um cálculo lambda digitado, do qual a maioria das linguagens de programação funcionais são derivadas, funções de ordem superior que assumem uma função como argumento são valores com tipos do formato.
</p>


<img src="https://latex.codecogs.com/gif.latex?({T_1}->{T_2})->{T_3}" /> 


#### Exemplos
##### Javascript

```js
function test(){
	const y = (f, x) => f(f(x));
	const z = x => x + 3;
	y(z, 7); // 13
}
```
## Arrow Functions

As funções de seta permitem uma sintaxe curta para escrever expressões de função.
Você não precisa da functionpalavra - chave, da returnpalavra - chave e dos colchetes .

###### ES5
```js
var x = function(x, y) {
   return x * y;
}
```
###### ES6
```js
const x = (x, y) => x * y;
ou
const x = (x, y) => { return x * y };
```

## Métodos e Operadores Práticos

#### Os métodos que veremos:
> 1. Spread operator
>
> 2. for…of iterator
>
> 3. includes()
>
> 4. some()
>
> 5. every()
>
> 6. filter()
>
> 7. map()
>
> 8. reduce()

> Se você deseja se tornar um desenvolvedor web melhor, iniciar seu próprio negócio, ensinar outras pessoas ou melhorar suas habilidades de desenvolvimento, publicarei dicas e truques semanais nas mais recentes linguagens de desenvolvimento web. 


## Spread operator

O Operador de propagação **expande** uma matriz para seus elementos. Também pode ser usado para literais de objetos.

**Por que devo usá-lo?**

- É uma maneira simples e rápida de mostrar os itens de uma matriz
- Funciona para matrizes e literais de objetos
- É uma maneira rápida e intuitiva de passar argumentos
- Requer apenas três pontos…

**Exemplo:**
digamos que você queira mostrar uma lista de alimentos favoritos sem criar uma função de loop. Use um operador de spread como este:

```js
const products = ['A', 'B', 'C'];
console.log(...products);
// A B C
```


## Rest

A sintaxe de **rest parameter (parâmetros rest)** nos permite representar um número indefinido de argumentos como um array. 

```
function(a, b, ...theArgs) {
  // ...
}
```

Se o último argumento nomeado de uma função tiver prefixo com  `...`, ele irá se tornar um array em que os elemento de 0 (inclusive) até theArgs.length (exclusivo) são disponibilizados pelos argumentos atuais passados à função.

No exemplo acima, `theArgs` irá coletar o terceiro argumento da função (porquê o primeiro é mapeado para `a`, e o segundo para `b`) e assim por diante em todos os argumentos consecutivos.

### Diferença entre *rest parameters* e *`arguments` object*

Há três diferenças principais entre *rest parameters* e os [`arguments`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments) objects:

- *rest parameters* são os únicos que não foram atribuidos a um nome separado, enquanto os `arguments` object contêm todos os argumentos passados para a função;
- o objeto `arguments` não é um array, enquanto rest parameters são instâncias [`Array`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array), isso significa que métodos como [`sort`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort), [`map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map), [`forEach`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach) ou [`pop`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop) podem ser aplicados diretamente;
-  o objeto `arguments` possui a funcionalidade adicional de especificar ele mesmo (como a propriedade `callee`). 

###  De arguments para array 

 Rest parameters foram criados para reduzir o código padrão que foi induzida pelos argumentos 

```js
// Antes rest parameters, o seguinte codigo pode ser encontrado
function f(a, b){
  var args = Array.prototype.slice.call(arguments, f.length);
  // ...
}

// esse é o equivalente
function(a, b, ...args) {  
}
```

#### **Exemplos**

 Como `theArgs` é um array, você pode pegar número de elementos usando a propriedade `length`: 

```js
function fun1(...theArgs) {
  console.log(theArgs.length);
}
fun1();  // 0
fun1(5); // 1
fun1(5, 6, 7); // 3
```

No próximo exemplo, nós usamos o rest parâmetro para buscar argumentos do segundo parâmetro para o fim. Nós multiplicamos eles pelo primeiro parâmetro: 

```js
function multiply(multiplier, ...theArgs) {
  return theArgs.map(function (element) {
    return multiplier * element;
  });
}
var arr = multiply(2, 1, 2, 3); 
console.log(arr); // [2, 4, 6]
```

 O próximo exemplo mostra como você pode usar metodos do Array em rest params, mas não no objeto `arguments`: 

```js
function sortRestArgs(...theArgs) {
  var sortedArgs = theArgs.sort();
  return sortedArgs;
}
console.log(sortRestArgs(5,3,7,1)); // Exibe 1,3,5,7

function sortArguments() {
  var sortedArgs = arguments.sort(); 
  return sortedArgs; // isso nunca irá ocorrer
}
// throws a TypeError: arguments.sort is not a function
console.log(sortArguments(5,3,7,1));
```

 a fim de usar o objeto `arguments`, você precisará converte-lo para um array antes. 


## for…of iterator

A `for...of`instrução faz um loop / itera pela coleção e fornece a capacidade de modificar itens específicos. Ele substitui a maneira convencional de fazer a `for-loop`.

**Por que devo usá-lo?**

- É uma maneira simples de adicionar ou atualizar um item
- Para realizar cálculos (soma, multiplicação etc.)
- Ao usar instruções condicionais (se, enquanto, alternar etc.)
- Leva a código limpo e legível

**Exemplo:**
digamos que você tenha uma caixa de ferramentas e deseje mostrar todas as ferramentas dentro dela. O `for...of`iterador facilita.

```js
const categorias = ['Smartphones', 'Tables', 'Notebooks']
for(const item of categorias){
    console.log(item);
}
// Smarhphones
// Tablets
// Notebooks
```

## Includes()  method

O `includes()`método é usado para verificar se existe uma sequência específica em uma coleção e retorna `true`or `false`. Lembre-se de que faz distinção entre maiúsculas e minúsculas: se o item dentro da coleção for `SCHOOL`e você procurar `school`, ele retornará `false`.

**Por que devo usá-lo?**

- Para criar uma funcionalidade de pesquisa simples
- É uma abordagem intuitiva para determinar se existe uma string
- Ele usa instruções condicionais para modificar, filtrar e assim por diante
- Leva ao código legível

**Exemplo:**
digamos que, por qualquer motivo, você não esteja ciente de quais carros você tem na garagem e você precisa de um sistema para verificar se o carro que você deseja existe ou não. `includes()`para o resgate!

```js
const marcas = ['BMW', 'AUDI', 'MERCEDEZ'];
const buscarMarca = marcas.includes('BMW');
console.log(buscarMarca);
// true
```

## Some() method

O `some()`método verifica se existem alguns elementos em uma matriz e retorna `true`ou `false`. Isso é um pouco semelhante ao conceito do `includes()`método, exceto que o argumento é uma função e não uma string.

**Por que devo usá-lo?**

- Garante que **algum** item passe no teste
- Ele executa instruções condicionais usando funções
- Torne seu código declarativo
- Alguns são bons o suficiente

**Exemplo:**
digamos que você seja proprietário de um clube e não se importe com quem entra no clube. Mas alguns não podem entrar porque estão bebendo demais (minha criatividade no seu melhor). Confira as diferenças entre ES5 e ES6 abaixo:

#### **ES5**

```js
const idade = [16, 14, 18];
idade.some(function(pessoa)){
           return pessoa >= 18;
           });
// Output: true
```

#### **ES6**

```js
const idade = [16, 14, 18];
idade.some((pessoa) => pessoa >= 18);
// true
```



## Every() method

O `every()`método percorre a matriz, verifica todos os itens e retorna `true`ou `false`. Mesmo conceito que `some()`. Exceto que todo item deve satisfazer a declaração condicional, caso contrário, ele retornará `false`.

**Por que devo usá-lo?**

- Ele garante que **todos os** itens passem no teste
- Você pode executar instruções condicionais usando funções
- Torne seu código declarativo

**Exemplo:**
Na última vez em que você permitiu que `some()`estudantes menores de idade entrassem no clube, alguém denunciou isso e a polícia o pegou. Dessa vez, você não deixará isso acontecer e garantirá que **todos** passem o limite de idade com o `every()`operador.

#### **ES5**

```js
const idade = [17, 13, 18];
idade.every(function(pessoa){
return pessoa >= 18;
});
// Output: true
```

#### **ES6**

```js
const idade = [17, 13, 18];
idade.every((pessoa) => pessoa >= 18);
// true
```



## Filter() method

O `filter()`método cria uma nova matriz com todos os elementos que passam no teste.

A função filter é bem semelhante ao map: ela também recebe um callback como parâmetro e também retorna um novo array, a única diferença é que filter, como o próprio nome diz, retorna um filtro dos elementos do array inicial baseado na função de callback.

**Por que devo usá-lo?**

- Assim, você pode evitar alterar a matriz principal
- Permite filtrar itens desnecessários
- Fornece código mais legível

**Exemplo:**
suponha que você queira devolver apenas preços superiores ou iguais a 30. Filtre todos os outros preços…

#### **ES5**

```js
const precos = [25, 30, 28, 15, 50, 45, 22, 42];
idade.every(function(preco){
return preco >= 30;
});
// Output: {30, 42, 45, 50}
```

#### **ES6**

```js
const precos = [25, 30, 28, 15, 50, 45, 22, 42];
idade.every((preco) => preco >= 30);
// true
```

Imaginando que temos um array de inteiros e desejamos retornar apenas aqueles que são maiores do que 4. Podemos resolver assim usando o filter:

#### **ES5**

```js
var numbers = [1, 4, 7, 10];

var isBiggerThanFour = function(value) {
    return value > 4;
};

var numbersBiggerThanFour = numbers.filter(isBiggerThanFour); // [7, 10]
```

#### **ES6**

```js
const numbers = [1, 4, 7, 10];
const isBiggerThanFour = value => value > 4;

const numbersBiggerThanFour = numbers.filter(isBiggerThanFour); // [7, 10]
```

## Map() method

O `map()`método é semelhante ao `filter()`método em termos de retorno de uma nova matriz. No entanto, a única diferença é que ele é usado para modificar itens.

**Por que devo usá-lo?**

- Permite evitar alterações na matriz principal
- Você pode modificar os itens que deseja
- Fornece código mais legível

**Exemplo:**
digamos que você tenha uma lista de produtos com preços. Seu gerente precisa de uma lista para mostrar os novos preços depois de terem sido tributados em 25%. O `map()`método pode ajudá-lo.

#### **ES5**

```js
const listaDePrecos = [300, 280, 150, 450];
listaDePrecos.map(function(item){
return item * 0.75;
});
// Output: [225, 210, 112.5, 337.5]
```

#### **ES6**

```js
const listaDePrecos = [300, 280, 150, 450];
idade.every((item) => item * 0.75);
// [225, 210, 112.5, 337.5]
```

Nesse outro cenário abaixo, percebemos o reaproveitamento de código que podemos conseguir ao usar o map.
Possuímos dois arrays de objetos diferentes, porém ambos tem o campo name, e precisamos de uma função que retorne um novo array apenas com os names dos objetos:

#### **ES5**

```js
var students = [
    { name: 'Anna', grade: 6 },
    { name: 'John', grade: 4 },
    { name: 'Maria', grade: 9 }
];

var teachers = [
    { name: 'Mark', salary: 2500 },
    { name: 'Todd', salary: 3700 },
    { name: 'Angela', salary: 1900 }
];

var byName = function(object) {
    return object.name;
};

var byNames = function(list) {
    return list.map(byName);
};

byNames(students); // ["Anna", "John", "Maria"]
byNames(teachers); // ["Mark", "Todd", "Angela"]
```

#### **ES6**

```js
const students = [
    { name: 'Anna', grade: 6 },
    { name: 'John', grade: 4 },
    { name: 'Maria', grade: 9 }
];

const teachers = [
    { name: 'Mark', salary: 2500 },
    { name: 'Todd', salary: 3700 },
    { name: 'Angela', salary: 1900 }
];

const byName = object => object.name;
const byNames = list => list.map(byName);

byNames(students); // ["Anna", "John", "Maria"]
byNames(teachers); // ["Mark", "Todd", "Angela"]
```

## Reduce() method

Uma das funções que mais gera dúvidas é o reduce.

O `reduce()`método pode ser usado para transformar uma matriz em outra coisa, que pode ser um número inteiro, um objeto, uma cadeia de promessas (execução sequencial de promessas) etc. Por razões práticas, um caso de uso simples seria somar uma lista de números inteiros.
Em resumo, ele recebe como parâmetro um callback e um valor inicial, com o objetivo de "reduzir" o array a um único valor.

**Por que devo usá-lo?**

- Executar cálculos
- Calcular um valor
- Contar duplicatas
- Agrupar objetos por propriedade
- Executar promessas sequencialmente
- É uma maneira rápida de realizar cálculos

**Exemplo:**
digamos que você queira descobrir suas despesas totais por uma semana. Use `reduce()`para obter esse valor.

O cenário mais comum para explicar o reduce é uma soma:

#### **ES5**

```js
const despesas = [300, 280, 150, 450];
listaDePrecos.reduce(function(first, last){
return first + last;
});
// Output: [1180]
```
Outro Exemplo

```js
var numbers = [1, 2, 3];

var sum = function(x, y) {
    return x + y;
};

var numbersSum = numbers.reduce(sum, 0); // 6
```

#### **ES6**

```js
const despesas = [300, 280, 150, 450];
idade.reduce((first, last) => first + last);
// [1180]
```

Outro Exemplo

```js
const numbers = [1, 2, 3];
const sum = (x, y) => x + y;
const numbersSum = numbers.reduce(sum, 0); // 6
```
> O primeiro parâmetro é a função que será aplicada, no caso uma soma. 
> E o segundo parâmetro é o valor inicial. Se por algum motivo precisássemos começar a soma com 10, faríamos dessa forma:

Mas o reduce não serve apenas para somas, podemos também trabalhar com strings. Imaginando que nós temos um array de meses e precisamos retornar o meses dessa forma: JAN/FEV/MAR … / DEZ.
Podemos fazer assim:

#### **ES5**

```js
var months = ['JAN', 'FEV', 'MAR', /*...*/ , 'DEZ'];
var monthsShortener = function(previous, current) {
    return previous + '/' + current;
};

var shortenedMonths = months.reduce(monthsShortener, '');
// /JAN/FEV/MAR ... /DEZ
```

Nós queríamos isso: JAN/FEV/MAR … /DEZ
Mas obtivemos isso: /JAN/FEV/MAR … /DEZ

Função monthsShortener para adicionar uma condição que faça a prevenção desse erro:

```js
const months = ['JAN', 'FEV', 'MAR', /*...*/ , 'DEZ'];
const monthsShortener = (previous, current) => {
    if (previous === '') {
        return current;
    } else {
        return previous + '/' + current;
   }
};

const shortenedMonths = months.reduce(monthsShortener, '');
// JAN/FEV/MAR ... /DEZ
```

#### **ES6**

```js
const months = ['JAN', 'FEV', 'MAR', /*...*/ , 'DEZ'];

const monthsShortener = (previous, current) => {
    if (previous === '') {
        return current;
    } else {
        return previous + '/' + current;
   }
};

const shortenedMonths = months.reduce(monthsShortener, '');
// JAN/FEV/MAR ... /DEZ
```

## Currying

A técnica de transformar uma função com múltiplos parâmetros em uma sequência de funções que aceitam apenas um parâmetro é chamada de Currying.

Se na teoria ficou confuso, na prática seria transformar isso:

```js
var add = function(x, y) {
   return x + y;
};

add(1, 2) // 3
``` 

#### Nisso

```js
var add = function(x) {
    return function(y) {
        return x + y;
    };
};

add(1)(2); // 3
```

A princípio parece que estamos apenas adicionando mais dificuldade sem nenhum ganho. Porém temos uma grande vantagem: transformar 0 código em pequenos pedaços mais expressivos e com maior reuso.
Pensando em uma aplicação que possui diversos trechos do código uma soma com 5 e outra com 10, podemos usar a segunda versão da função add dessa forma:

```js
var addFive = add(5);
var addTen = add(10);

addFive(3); // 8
addFive(1); // 6

addTen(1); // 11
addTen(10); //20
```
Mais um exemplo seria um Hello World simples com uma curried function. Podemos implementá-lo desse jeito com ES5:

#### **ES5**

```js
var greeting = function(greet) {
    return function(name) {
        return greet + ' ' + name;
    };
};

var hello = greeting('Hello');
hello('World'); // Hello World
hello('Matheus'); // Hello Matheus
```

#### **ES6**

```js
const greeting = greet => name => greet + ' ' + name;
const hello = greeting('Hello');

hello('World'); // Hello World
hello('Matheus'); // Hello Matheus
```

## Compose

Podemos compor funções pequenas para gerar outras mais complexas de forma bem fácil em JavaScript. A vantagem é o poder de usar essas funções mais complexas, de forma simples, em toda aplicação. Ou seja, aumentamos o reuso.
Por exemplo, em uma aplicação em que necessitamos de uma função para transformar uma string passada pelo usuário em um grito: mudar para caracteres maiúsculos e adicionar uma exclamação no final. Podemos fazer assim em ES5:

#### **ES5**

```js
var compose = function(f, g) {
    return function(x) {
        return f(g(x));
    };
};

var toUpperCase = function(x) {
    return x.toUpperCase();
};

var exclaim = function(x) {
    return x + '!';
};

var angry = compose(toUpperCase, exclaim);

angry('ahhh'); // AHHH!
```

#### **ES6**

```js
const compose = (f, g) => x => f(g(x));

const toUpperCase = x => x.toUpperCase();
const exclaim = x => x + '!';

const angry = compose(toUpperCase, exclaim);

angry('ahhh'); // AHHH!
```




------

Global Ref:  https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Functions/rest_parameters 

