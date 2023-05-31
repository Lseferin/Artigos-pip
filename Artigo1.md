Materiais/fontes:<br>
https://blog.matheuscastiglioni.com.br/definindo-funcoes-em-javascript/ <br>https://sites.google.com/site/esdicapsi/funcoes 



Tópicos:<br>
-[Introdução](https://github.com/Lseferin/artigos/blob/main/Artigo1.md#introdu%C3%A7%C3%A3o)<br>
-[Quais vantagens do uso de função?](https://github.com/Lseferin/artigos/blob/main/Artigo1.md#quais-vantagens-do-uso-de-fun%C3%A7%C3%A3o)<br>
-[Estrutura básica de uma função](https://github.com/Lseferin/artigos/blob/main/Artigo1.md#estrutura-b%C3%A1sica-de-uma-fun%C3%A7%C3%A3o)<br>
-[Valor de retorno](https://github.com/Lseferin/artigos/blob/main/Artigo1.md#valor-do-retorno)<br>
-[Parâmetros](https://github.com/Lseferin/artigos/blob/main/Artigo1.md#par%C3%A2metros)<br>
-[Como utilizar uma função?](https://github.com/Lseferin/artigos/blob/main/Artigo1.md#-como-utilizar-uma-fun%C3%A7%C3%A3o)<br>
-[Escopo de função](https://github.com/Lseferin/artigos/blob/main/Artigo1.md#-escopo-de-fun%C3%A7%C3%A3o)<br>
-[Tipos de funções](https://github.com/Lseferin/artigos/blob/main/Artigo1.md#tipos-de-fun%C3%A7%C3%B5es)<br>
-[Recursividade](https://github.com/Lseferin/artigos/blob/main/Artigo1.md#extra-recursividade-)<br>
-[Considerações](https://github.com/Lseferin/artigos/blob/main/Artigo1.md#extra-recursividade-)<br>


<h1>Funções</h1>

<h2>Introdução:</h2>
Uma função encapsula trechos de códigos para que possam ser reutilizados em vários locais da aplicação. Para utilizar uma função, você deve defini-la em algum lugar do escopo onde quiser utilizá-la.


<h2>Quais vantagens do uso de função?</h2>
Um dos motivos para utilizar uma função é evitar a repetição de código, assim podendo apenas invocar o nome da função para fazer o reaproveitamento do código.
Outro motivo para utilizar seria o caso em que teríamos que alterar/ajustar algo da função, como a função se repete várias vezes na aplicação, desta forma precisamos alterar a função somente quando ela é desenvolvida e não em todas as vezes que for invocada. 

<h2>Estrutura básica de uma função:</h2>

Declaração de função: Para definirmos uma função, devemos iniciar com a palavra function, seguida pelo nome da função e opcionalmente uma lista de parâmetros entre parênteses. 

```
function funcao(params1, params2) {
	// ação da função
}
funcao(valorParams1, valorParams2)
```


No mundo real, em Javascript, teríamos:<br>
```
function soma(num1, num2) { 
	return (num1 + num2)
}
soma(1, 5) 
```


<h3>Valor do retorno:</h3>
Geralmente, uma função executa uma lógica e devolve o resultado desse procedimento. Esse retorno é feito através da instrução return, seguida do valor de retorno. 
Além dos tipos normais de valor (int, float, string…), podemos ter também o tipo especial void, que significa que não há valor de retorno. 
<br>
<br>
<strong>Alguns tipos de retorno</strong> 

<strong>String</strong><br>
```
function ola(){
	return "Olá"
}
console.log(ola())
```


<strong>Int</strong> 

```
function soma(num1, num2){
	return num1 + num2;
}
function calculadora(acao, numero1, numero2){
	var result = 0;
	switch(acao){
		case 'soma':
			result = soma(numero1, numero2)
		break;
		}
	return result;
}
calculadora('soma', 2, 5) => 7
```

<strong>Void</strong>

```
function ola(p1) {
	console.log(p1)
}
ola()
```


<h3>Parâmetros:</h3> 
O parâmetro é um valor fornecido à função quando chamada. Também podemos chamar os parâmetros de argumentos da função. 
Os parâmetros funcionam como variáveis locais e, para declará-los, adicionamos-os entre parênteses. 
Os parâmetros são usados apenas no escopo da própria função.  
No Javascript, os parâmetros não são obrigatórios. 

<h2>Tipos de funções</h2>
<h3> Função com um parâmetro</h3> 

```
function ola(p1) {
	console.log(p1)
}
var p1 = "Olá"
ola(p1)
```

<h3> Função com dois parâmetros</h3> 

```
function ola(p1, p2) {
	console.log(p1, p2)
}
ola("Olá", "Tudo bem?")
```


<h2> Como utilizar uma função?</h2> 


O nome da função é como ela será chamada no código quantas vezes forem necessárias;
A ação da função é o que será executado quando a função for chamada, podendo ser um console.log que seria a impressão de algo, alguma lógica com laço de repetição ou estruturas condicionais. 

<h2> Escopo de função:</h2> 
Quando uma variável ou função é declarada em um determinado escopo, ela só pode ser acessada dentro daquele escopo ou de escopos internos a ele.


<h2> Tipos de funções:</h2> 

Função anônima: função que não possui nomenclatura. Geralmente são usadas como argumentos de uma outra função.
Função sem parâmetros e sem retorno.

```
function ola() {
	console.log("Olá")
}
 ola()
 ```


<h3> Função sem parâmetro e com retorno.</h3>

```
function ola() {
	return "Olá"
}
console.log(ola())
```


<h3>Função com parâmetro e sem retorno.</h3>


```
function ola(nome) {
	console.log("Olá")
}
ola()
```


<h3>Função com parâmetro e com retorno. </h3>

```
function ola(nome) {
	return nome)
}
ola("Lívia")
```



<strong>Com retorno: Significa que a função tem um retorno de tipo int, float, char, etc.</strong>

<strong>Exemplo:</strong><br>

```
function ola() {
	return "Olá"
} 
console.log(ola())
```


<h3>Arrow Function:</h3> <br>Uma arrow function possui uma estrutura mais curta e objetiva que uma função normal. Possuem um retorno implícito, retornando valores sem o uso do return. <br>
<strong>Exemplo:</strong><br> 

```( ) => expressao; (parametros) => expressao; ( ) => { } ```

Obs: Se o retorno possuir apenas uma linha de código, não é necessário o uso das chaves, caso contrário o uso das chaves é obrigatório. 

<h3>Função assíncrona:</h3><br> Uma função assíncrona pode conter a palavra reservada await, que pausa a execução do script e espera uma resolução da promise (promessa) passada, após isso, retorna a execução da função e retorna o valor resolvido. 


```
async function getData() {
  let response = await fetch('http://apiurl.com');
}
```

<strong>ref:</strong> https://www.freecodecamp.org/portuguese/news/tutorial-de-async-e-await-em-javascript-como-aguardar-que-uma-funcao-se-encerre-em-js/


<h2>Extra: Recursividade: </h2>
Durante o estudo, identifiquei o uso de funções recursivas. Recursão pode ser considerado um processo de repetição, desta forma podemos dizer que a recursividade na programação é quando a função chama a si mesma, de forma direta ou indireta. Porém, devemos tomar cuidado para que isto não ocasione um loop, que seria quando uma parte do código se repete eternamente, ocasionando o travamento do sistema.
 
<strong>Exemplo:</strong>

```function countDown(fromNumber, toNumber) {
  if (fromNumber > toNumber) {
	console.log(fromNumber);
	countDown(fromNumber-1, toNumber);
	}
} countDown(3, -20)
```


<h2>Considerações:</h2>
 Com isso, aprendemos um pouco mais sobre funções, seus tipos e quando usá-las. 




