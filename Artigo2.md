Materiais/fontes: <br>
https://www.alura.com.br/artigos/react-js<br>
https://blog.geekhunter.com.br/criando-componentes-react-componentes-de-classe-e-funcional-sem-estado/#:~:text=de%20componentes%20React-,O%20que%20s%C3%A3o%20componentes%20React%3F,elementos%20React%2C%20os%20chamados%20JSX.<br>

Tópicos: <br>
-[O que é o React?](https://github.com/Lseferin/Artigos-pip/blob/main/Artigo2.md#o-que-%C3%A9-o-react)<br>
-[React e React Native](https://github.com/Lseferin/Artigos-pip/blob/main/Artigo2.md#react-e-react-native)<br>
-[Requisitos para aprender React](https://github.com/Lseferin/Artigos-pip/blob/main/Artigo2.md#requisitos-para-aprender-react)<br>
-[Como funciona o componente?](https://github.com/Lseferin/Artigos-pip/blob/main/Artigo2.md#como-funciona-o-componente)<br>
-[Tipos de componentes](https://github.com/Lseferin/Artigos-pip/blob/main/Artigo2.md#tipos-de-componentes)<br>
-[O que são estados?](https://github.com/Lseferin/Artigos-pip/blob/main/Artigo2.md#o-que-s%C3%A3o-estados-no-react)<br>
-[Props](https://github.com/Lseferin/Artigos-pip/blob/main/Artigo2.md#props)<br>
-[Quando usar?](https://github.com/Lseferin/Artigos-pip/blob/main/Artigo2.md#quando-usar-)<br>
-[Como usar?](https://github.com/Lseferin/Artigos-pip/blob/main/Artigo2.md#como-usar-um-componente)
-[Considerações](https://github.com/Lseferin/Artigos-pip/blob/main/Artigo2.md#considera%C3%A7%C3%B5es)<br>

<h1>Componentes do React</h1>

<h2>O que é o React?</h2>
O React é um framework Javascript, criado pelo Facebook (atual Meta), com o foco em criar interfaces. Um dos principais usos do React é para a criação de aplicações web complexas e que precisam ser atualizadas em tempo real. O React é um dos Framework mais populares e atualizados de todo o mundo. E oferece muitos recursos e ferramentas úteis que tornam o desenvolvimento mais fácil. Incluindo bibliotecas de componentes prontos para uso. 

<h2>React e React Native</h2>
Muito se confunde React e React Native, mas a sua principal diferença é que React é usado na criação de aplicações web, enquanto o React Native é usado na criação de aplicações mobile.

<h2>Requisitos para aprender React</h2>
Como o React é uma biblioteca Javascript, para aprender React é necessário ter conhecimento do Javascript. Incluindo saber entender sobre variáveis, loops, funções e condicionais. Também deve ter familiaridade com HTML e CSS, pois é necessário saber estilizar um documento HTML. 

<h2>Como funciona o componente?</h2>
O React é usado para a criação de componentes  que são pedaços de código que representam uma parte específica da interface de uma aplicação. Cada componente tem um estado, que é uma variável que armazena informações que mudam dentro do componente. Quando o usuário interage com a aplicação, o estado dos componentes é atualizado. O React também utiliza o Virtual DOM (Document Object Model Virtual)(3), que é uma representação em memória da interface do aplicativo. Quando o estado do componente muda, o Virtual DOM é atualizado e comparado com o DOM real para determinar quais mudanças precisam ser feitas na interface.  

<h2>Tipos de Componentes</h2>

<h3>Componentes de classe:</h3>
São componentes que possuem alto nível de poder dentro da aplicação, além de gerenciar o próprio estado, lidam com partes lógicas da aplicação e manipulam eventos através de métodos.<br>
  <strong>Exemplo:</strong>

```
import React from "react";

interface Props {
  name: string;
} 

function Componente ({
  name,
}: Props {

  return (
	return <h3>Olá, {name}</h3>
  )
}  

export default Componente;
```


  <h3>Componentes funcionais:</h3>
É um tipo de componente que em vez de usar uma classe, ele é apenas uma função que recebe as propriedades como argumento e retorna o elemento React.  <br>
  <strong>Exemplo:</strong>

  ```
function Titulo(props) {
	return <h1>{props.texto}</h1>;
}
```

<h2>O que são estados no react?</h2>
Os estados são uma forma de guardar informações dentro do componente. Representam valores renderizados, ou seja, que estão atualmente na tela. 

```
// components/Lista.js

import React from 'react';
import Post from 'Post';

class Lista extends React.Component {
  state = {
    posts: [
      { id: 1, title: "Título 1" },
      { id: 2, title: "Título 2" },
      { id: 3, title: "Título 3" }
    ],
  };

  render() {
    ...
  }
}
```

<strong>Ref:</strong> https://blog.rocketseat.com.br/react-do-zero-componentizacao-propriedades-e-estado/
<h2>Props:</h2>
São usadas para passar dados entre componentes. A diferença entre prop e estado é que as informações que são passadas para um estado, são tratadas dentro do componente, e das props são tratadas fora do componente. 

```
// components/Post.js

import React from 'react';

class Post extends React.Component {
  render() {
    return <h1>{this.props.title}</h1>;
  }
}
```

<strong>Ref:</strong> https://blog.rocketseat.com.br/react-do-zero-componentizacao-propriedades-e-estado/

<h3>Quando usar? </h3>
O componente de classe é algo mais funcional, que apresenta dados que possam variar, enquanto o componente funcional sem estado é algo mais para apenas mostrar a informação sem variação.

Para a criação de um componente que exibe avatar do usuário, exibir posts, criar tabela para exibir lista de dados e exibição de um loader, usamos componente funcional sem estado. Já para criar um componente de dropdown, uma busca ou um componente que valide os dados de um formulário, nós usamos componente de classe.
Exemplos de código de um componente React:
Como criar um componente:

```
import React from "react";
//imports

interface Props {
  name: string;
  status?: boolean;
} 
//interface de props com a prop e tipagem dela
//símbolo de interrogação (?) significa que a prop é opcional

function Componente ({
  name,
  status = true,
//chamada do componente com as props e valores iniciais setados
}: Props {

  return (
//return com a estrutura do componentes, podendo conter outros componentes dentro
//para incluir outro componente dentro deste arquivo, basta importá-lo no trecho de imports e chamá-lo quando for necessário
  )
}  

export default Componente;
```

<h3>Como usar um componente:</h3>

```
import React from "react";
import Componente from "./Componente";

interface Props2 {
status?: boolean,
}

function Componente2 ({
	status = true, 
}: Props2) {

return (
	<Componente
name="Teste"
/>
  )
}
export default Componente2;
```

<h2>Considerações:</h2>
A composição do componente é combinar pequenas funções para criar algo maior, assim como combinar componentes para criar um outro componente mais completo e funcional. 





