Materiais/fontes:
https://www.redhat.com/pt-br/topics/api/what-are-application-programming-interfaces#:~:text=API%20%C3%A9%20a%20 sigla%20em,cria%C3%A7%C3%A3o%20de%20aplica%C3%A7%C3%B5es%20de%20software.
https://www.devmedia.com.br/trabalhando-com-api/
https://www.devmedia.com.br/consumindo-uma-api-em-react-native/42837
https://santodigital.com.br/apis-nas-empresas-entenda-4-beneficios-que-elas-podem-trazer/



Tópicos:<br>
-[O que é uma API?](https://github.com/Lseferin/Artigos-pip/edit/main/Artigo3.md#o-que-%C3%A9-uma-api-)<br>
-[Como funciona?](https://github.com/Lseferin/Artigos-pip/edit/main/Artigo3.md#como-funciona)<br>
-[Caso de uso:](https://github.com/Lseferin/Artigos-pip/edit/main/Artigo3.md#caso-de-uso)<br>
-[Vantagens](https://github.com/Lseferin/Artigos-pip/edit/main/Artigo3.md#vantagens-de-usar-api)<br>
-[Como consumir uma API](https://github.com/Lseferin/Artigos-pip/edit/main/Artigo3.md#como-consumir-uma-api)<br>
-[Padrões de API](https://github.com/Lseferin/Artigos-pip/edit/main/Artigo3.md#padr%C3%B5es-de-api)<br>
-[API remota](https://github.com/Lseferin/Artigos-pip/edit/main/Artigo3.md#api-remota)<br>
-[API web](https://github.com/Lseferin/Artigos-pip/edit/main/Artigo3.md#api-web)<br>
-[GraphQL](https://github.com/Lseferin/Artigos-pip/edit/main/Artigo3.md#graphql)<br>

<h1>Consumo de API</h1>

<h2>O que é uma API? </h2>
A sigla Application Programming Interface é um conjunto de definições e protocolos para a criação de aplicações. Pode ser pensada como um contrato de serviço entre duas aplicações. 

<h2>Como funciona?</h2>
O seu serviço pode se comunicar com outros produtos sem precisar saber a forma que foram implementados, desta forma simplifica o desenvolvimento da aplicação. A API funciona como se fosse um contrato, com seus dados que representam um acordo entre as aplicações. Quando uma dessas aplicações envia uma solicitação remota, isso acaba determinando como a outra aplicação irá responder. 

<h2>Caso de uso:</h2>
Um bom exemplo para o uso de uma API é a criação de uma aplicação meteorológica, onde será exibida a previsão do tempo para que o usuário possa consultar as condições climáticas de seu local, ou então uma aplicação que tenha pagamento por cartão de crédito. Em ambos os casos precisamos de uma API para consultar as informações/serviços para que tenhamos os dados necessários para criarmos nossa aplicação de forma completa e funcional. 

<h2>Vantagens de usar API</h2>
Ajuda na reestruturação de sistemas internos
Melhora a experiência do usuário
Permite a conectividade com parceiros

<h2>Como consumir uma API:</h2>
<h3>Fetch</h3>
Para consumirmos os dados de uma API, utilizamos o método chamado fetch.

```
fetch('https://api.github.com/users/lseferin');
```

O código acima envia uma requisição para a URL passada. Esperamos receber os dados com esta requisição. 

```
fetch('https://api.github.com/users/lseferin') .then( (resposta) => resposta.json())
```

Usamos o método then para receber os dados.
Dentro do método then, temos uma função que é executada quando o fetch recebe o retorno da API. 

```
(resposta) => resposta.json()
```

A função dentro de then, recebe uma resposta e tenta converter para JSON através do método .json().



```
1- fetch('https://api.github.com/users/lseferin')
2-  .then( (resposta) => {return resposta.json()})
3-  .then( ( json ) => console.log(json) )
4-  .catch( ( error ) => console.error(error) )
```


Após executar o método .json(), chamamos uma função utilizando o then. Caso a tentativa de converter a resposta gere um erro queremos que a função catch seja executada.
<h3>Entendendo o código Fetch:</h3>

<strong>Linha 1:</strong> Enviamos uma requisição através do método fetch.<br>
<strong>Linha 2:</strong> Quando recebermos a resposta da requisição, a função dentro de then será executada. Essa função recebe a resposta da API e tenta convertê-la para JSON.<br>
<strong>Linha 3:</strong> Caso o método .json() execute sem gerar erro, a função dentro de then será executada.<br>
<strong>Linha 4:</strong> Caso o método .json() gere um erro, a função dentro do método catch será executada.<br>
<h3>Axios</h3>
Axios é uma biblioteca que permite a integração do projeto com qualquer API. Uma das principais causas de se usar Axios é pela sua capacidade de interceptar requisições, que é útil quando precisamos examinar ou alterar essas requisições. 

<h3>Sintaxe em Axios:</h3>

```
1- axios.get('https://api.github.com/users/lseferin')
2-  .then(function (response) {
3-  console.log(response.data);
4- })
5-  .catch(function (error) {
6-  console.log(error);
})
```

<h3>Entendendo o código em Axios:</h3>
<strong>Linha 1:</strong> Uma requisição é feita através do método axios.get.<br>
<strong>Linha 2:</strong> Quando recebermos a resposta da requisição, a função dentro de then será executada. Essa função recebe a resposta da API.<br>
<strong>Linha 3:</strong> Console.log imprimindo as respostas vindas da requisição.<br>
<strong>Linha 5:</strong> Caso ocorra algum erro, a função dentro do método catch será executada.<br>
<strong>Linha 6:</strong> Console.log exibindo o erro <br>
<h2>Padrões de API</h2>
<h3>Rest:</h3> Rest é um padrão de arquitetura, um conjunto de regras que são aplicadas em uma API, para tornar a utilização segura e padronizada.
<h3>RESTful:</h3> É uma interface que os sistemas usam para trocar informações de forma segura. Quando a API é RESTful, significa que ela aplica os princípios propostos por Rest. 

<h2>API Remota</h2>
As APIs remotas interagem por meio de uma rede de comunicações, ou seja, um lugar fora do computador que está realizando a solicitação. A rede de comunicação mais usada é a internet, sendo assim, a maioria das APIs são feitas com base em padrões da web. Sendo assim, nem todas as APIs remotas são web, mas podemos dizer que todas as APIs web são remotas.

<h2>API Web</h2>
APIs web normalmente usam protocolo HTTP para solicitações e fornecem uma definição da estrutura das respostas. Estas respostas geralmente são do formato XML ou JSON. Estes formatos são preferência, pois apresentam os dados de forma simplificada e facilitam a manipulação por outras aplicações. 

<h2>GraphQL</h2>
O GraphQL é uma linguagem de consulta e ambiente de execução Rest. Ele tem como prioridade fornecer os dados que o cliente solicita. Também permite que os desenvolvedores extraiam dados de várias fontes em uma única chamada da API. 
