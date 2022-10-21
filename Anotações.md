# AULA 01

- Vite é um bundler, que nada mais é do que uma ferramenta que é capaz de pegar diversos tipos de arquivos (css, jpg, javascript, html) e depois empacota tudo isso para que ele possa ser usado depois
  - Serve para ter mais dinamismo na hora de programar
  - Adicionar a ideia de import (css, imagens)
  - Para baixar ele podemos utilizar ````npm create vite@latest```, no nosso caso estamos usando o Vannila
  - Agora precisamos instalar o node ````npm install```
- Executar o ````npm run dev``` para abrir o projeto na web

**DOM**

- Document Object Model
- Representaçao do HTML em objetos JavaScript: Atributos(propriedades) e métodos (funcionalidades)
- Criado pelo navegador: É uma interface (API) usada no navegador
- JS usa a DOM para se conectar ao HTML
  - DOM não é o JavaScript
- Manipular HTML com JavaScript
  - Modificar o HTML, os estilos e até disparar ações

# AULA 02

- Para realizar as validações dos campos vamos utilizar o IMask.js que é uma biblioteca [https://imask.js.org]
  - ```npm install imask```

**Expressões regulares**

- Conhecida como Regular Expression ou Regex, é uma tecnologia usada para buscar padrões dentro de textos e funciona em diversas linguagens.
-> Como pensar?
- Existe uma maneira correta de pensar ao utilizar essa tecnologia para a busca de padrões
  * Leitura da esquerda para direita
  * Ler um caractere de cada vez, um após ao outro
  * Conhecer os caracteres reservado da tecnologia
```javascript

  const re = /foo/;
  const re = new RegExp(/foo/);
```
- Podemos executar elas através da ferramenta de pesquisa do Visual Studio Code
  ```Javascript
  //Agrupa os padrões em um array
  const matches = 'aBC'.match(/[A-Z]/g);
  // Array [B, C]

  //Pesquisa se existe ou não o padrão
  const index = 'aBC'.search(/[A-Z]/);
  // 1

  //Substitui os padrões pelo valor
  const next = 'aBC'.replace(/a/, 'A');
  // ABC
  
  
  ```

**Fazer regra dos cartões Visa e Mastercard**

-> Visa: inicia com 4 seguido de mais 15 dígitos
  ```^4\d{0,15}```
-> Master:
  - Inicia com 5, seguido de um dígito entre 1 e 5, seguido de mais 2 dígitos
  - Inicia com 22, seguido de um dígito entre 2 e 9, seguido de mais 1 dígito
  - Inicia com 2, seguido de um dígito entre 3 e 7, seguido de mais 2 dígitos seguido de mais 12 dígitos
  ```(^5[1-5]\d{0,2} | ^22[2-9]\d | ^2[3-7]\d{0,2}\d{0,12})```

**Usando o Mask com exprssões regulares**

- Vamos utilizar o Dynamic Mask, ele vai permitir que possamos criar mais de uma mascara para cada elemento
- O ```dispatch: function(appended, dynamicMasked)``` vai servir para toda hora que a gente clicar no teclado a função ser chamada

# AULA 03

- Fazer o botão não recarregar a página
- Alterar o nome de forma dinâmica

**Eventos do IMask**
-> Obtendo e exibindo o CVC do cartão
  - Vamos pegar a mascara feita pelo Maykao e atribuir um evento a variavel, só que com o IMask
-> Obtendo e exibindo o número do cartão

```git remote set-url origin https://github.com/Henrriky/explorer-lab-01.git```
```git add.``` -> Pega todo o projeto e adiciona o projeto em um pacote