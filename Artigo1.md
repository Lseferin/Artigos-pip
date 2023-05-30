Materiais/fontes:<br>
https://blog.matheuscastiglioni.com.br/definindo-funcoes-em-javascript/ <br>https://sites.google.com/site/esdicapsi/funcoes 



Tópicos:<br>
Introdução<br>
Quais vantagens do uso de função?<br>
Estrutura básica de uma função<br>
Declaração<br>
Valor de retorno<br>
Tipos de funções<br>
Parâmetros<br>
Como utilizar uma função?<br>
Escopo de função<br>
Tipos de funções<br>
Recursividade<br>
Considerações<br>


<h1>Funções</h1>

<h2>Introdução:</h2>
Uma função encapsula trechos de códigos para que possam ser reutilizados em vários locais da aplicação. Para utilizar uma função, você deve defini-la em algum lugar do escopo onde quiser utilizá-la.


<h2>Quais vantagens do uso de função?</h2>
Um dos motivos para utilizar uma função é evitar a repetição de código, assim podendo apenas invocar o nome da função para fazer o reaproveitamento do código.
Outro motivo para utilizar seria o caso em que teríamos que alterar/ajustar algo da função, como a função se repete várias vezes na aplicação, desta forma precisamos alterar a função somente quando ela é desenvolvida e não em todas as vezes que for invocada. 

<h2>Estrutura básica de uma função:</h2>

Declaração de função: Para definirmos uma função, devemos iniciar com a palavra function, seguida pelo nome da função e opcionalmente uma lista de parâmetros entre parênteses. 

`function funcao(params1, params2) {`
<br>
	`// ação da função`
  <br>
`}`
<br>
`funcao(valorParams1, valorParams2)`



No mundo real, em Javascript, teríamos:<br>
`function soma(num1, num2) { `
<br>
	`return (num1 + num2)`
  <br>
`}`
<br>
`soma(1, 5) `


<h3>Valor do retorno:</h3>
Geralmente, uma função executa uma lógica e devolve o resultado desse procedimento. Esse retorno é feito através da instrução return, seguida do valor de retorno. 
Além dos tipos normais de valor (int, float, string…), podemos ter também o tipo especial void, que significa que não há valor de retorno. 
<br>
<br>
<strong>Alguns tipos de retorno</strong> 

String<br>
`function ola(){`
<br>
	`return "Olá"`
  <br>
`}`
<br>
`console.log(ola())`


<strong>Int</strong> 

`function soma(num1, num2){`
<br>
	`return num1 + num2;`
  <br>
`}`
<br>
`function calculadora(acao, numero1, numero2){`
<br>
`	var result = 0;`
<br>
	`switch(acao){`
  <br>
		`case 'soma':`
    <br>
			`result = soma(numero1, numero2)`
      <br>
		`break;`
    <br>
		`}`
    <br>
	`return result;`
  <br>
`}`
<br>
`calculadora('soma', 2, 5) => 7`
<br>

<strong>Void</strong>

`function ola(p1) {`
<br>
	`console.log(p1)`
  <br>
`}`
<br>
`ola()`
<br>


<h3>Parâmetros:</h3> 
O parâmetro é um valor fornecido à função quando chamada. Também podemos chamar os parâmetros de argumentos da função. 
Os parâmetros funcionam como variáveis locais e, para declará-los, adicionamos-os entre parênteses. 
Os parâmetros são usados apenas no escopo da própria função.  
No Javascript, os parâmetros não são obrigatórios. 

<h3> Função com um parâmetro</h3> 

`function ola(p1) {`
<br>
	`console.log(p1)`
  <br>
`}`
<br>
`var p1 = "Olá"`
<br>
`ola(p1)`
<br>

<h3> Função com dois parâmetros</h3> 

`function ola(p1, p2) {`
<br>
	`console.log(p1, p2)`
  <br>
`}`
<br>
`ola("Olá", "Tudo bem?")`
<br>


<h2> Como utilizar uma função?</h2> 


O nome da função é como ela será chamada no código quantas vezes forem necessárias;
A ação da função é o que será executado quando a função for chamada, podendo ser um console.log que seria a impressão de algo, alguma lógica com laço de repetição ou estruturas condicionais. 

<h2> Escopo de função:</h2> 
Quando uma variável ou função é declarada em um determinado escopo, ela só pode ser acessada dentro daquele escopo ou de escopos internos a ele.


<h2> Tipos de funções:</h2> 

Função anônima: função que não possui nomenclatura. Geralmente são usadas como argumentos de uma outra função.
Função sem parâmetros e sem retorno.

`function ola() {`
<br>
	`console.log("Olá")`
  <br>
`}`
<br>
 `ola()`
 <br>


<h3> Função sem parâmetro e com retorno.</h3>

`function ola() {`
<br>
	`return "Olá"`
  <br>
`} `
<br>
`console.log(ola())`
<br>


<h3>Função com parâmetro e sem retorno.</h3>


`function ola(nome) {`
<br>
	`console.log("Olá")`
  <br>
`}`
<br>
`ola()`
<br>


<h3>Função com parâmetro e com retorno. </h3>

`function ola(nome) {`
<br>
	`return nome)`
  <br>
`} `
<br>
`ola("Lívia")`
<br>



<strong>Com retorno: Significa que a função tem um retorno de tipo int, float, char, etc.</strong>

<strong>Exemplo:</strong><br>

`function ola() {`
<br>
	`return "Olá"`
  <br>
`}` 
<br>
`console.log(ola())`
<br>


<h3>Arrow Function:</h3> <br>Uma arrow function possui uma estrutura mais curta e objetiva que uma função normal. Possuem um retorno implícito, retornando valores sem o uso do return. <br>
<strong>Exemplo:</strong><br> 

`( ) => expressao; (parametros) => expressao; ( ) => { } `

Obs: Se o retorno possuir apenas uma linha de código, não é necessário o uso das chaves, caso contrário o uso das chaves é obrigatório. 

<h3>Função assíncrona:</h3><br> Uma função assíncrona pode conter a palavra reservada await, que pausa a execução do script e espera uma resolução da promise (promessa) passada, após isso, retorna a execução da função e retorna o valor resolvido. 


`async function getData() {`
<br>
  `let response = await fetch('http://apiurl.com');`
  <br>
`}`
<br>

<strong>ref:</strong> https://www.freecodecamp.org/portuguese/news/tutorial-de-async-e-await-em-javascript-como-aguardar-que-uma-funcao-se-encerre-em-js/


<h2>Extra: Recursividade: </h2>
Durante o estudo, identifiquei o uso de funções recursivas. Recursão pode ser considerado um processo de repetição, desta forma podemos dizer que a recursividade na programação é quando a função chama a si mesma, de forma direta ou indireta. Porém, devemos tomar cuidado para que isto não ocasione um loop, que seria quando uma parte do código se repete eternamente, ocasionando o travamento do sistema.
 
<strong>Exemplo:</strong>

`function countDown(fromNumber, toNumber) {`
<br>
  `if (fromNumber > toNumber) {`
  <br>
	`console.log(fromNumber);`
  <br>
	`countDown(fromNumber-1, toNumber);`
  <br>
`}`
<br>
`} countDown(3, -20)`
<br>


<h2>Considerações:</h2>
 Com isso, aprendemos um pouco mais sobre funções, seus tipos e quando usá-las.