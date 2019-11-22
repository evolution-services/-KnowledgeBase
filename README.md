## Classes no ES6

<p align="justify">
Uma classe é um tipo de função, mas, em vez de usar a palavra function- chave para iniciá-la, usamos a palavra-chave classe as propriedades são atribuídas dentro de um constructor() método.
</p>
<p align="justify">
Use a palavra class- chave para criar uma classe e sempre adicione um método construtor.
</p>
<p align="justify">
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

## Higher-Order Functions

#### Função de Ordem Superior

<p align="justify">
Em matemática e ciências da computação, uma função de ordem superior é uma função que executa pelo menos um dos seguintes procedimentos: assume uma ou mais funções como argumentos (ou seja, parâmetros processuais), retorna uma função como resultado.
Todas as outras funções são de primeira ordem. Em matemática, funções de ordem superior também são denominadas operadores ou funcionais. O operador diferencial no cálculo é um exemplo comum, pois mapeia uma função para sua derivada, também uma função. Funções de ordem superior não devem ser confundidas com outros usos da palavra "functor" ao longo da matemática.
</p>

<p align="justify">	
	<b>Functor: </b> <i>(em teoria das categorias, é um mapeamento entre categorias que preserva estruturas).</i>
</p>

<p align="justify">
No cálculo lambda sem tipo, todas as funções são de ordem superior; em um cálculo lambda digitado, do qual a maioria das linguagens de programação funcionais são derivadas, funções de ordem superior que assumem uma função como argumento são valores com tipos do formato.
</p>

![equation](https://latex.codecogs.com/gif.latex?({T_1}->{T_2})->{T_3})

#### Exemplos
##### Javascript

```javascript
function test(){
	const y = (f, x) => f(f(x));
	const z = x => x + 3;
	y(z, 7); // 13
}
```
##### C(#)
```C#
Func<Func<int,int>,Func<int,int>> twice = f => x => f(f(x));
	Func<int,int> y = x => x + 3;
	Console.WriteLine(twice(y)(7)); // 13
}
```
## Arrow Functions

As funções de seta permitem uma sintaxe curta para escrever expressões de função.

Você não precisa da functionpalavra - chave, da returnpalavra - chave e dos colchetes .

###### ES5
```
var x = function(x, y) {
   return x * y;
}
```
###### ES6
```
const x = (x, y) => x * y;
ou
const x = (x, y) => { return x * y };
```
