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
