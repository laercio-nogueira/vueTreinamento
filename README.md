## Criar e configurar um projeto em vue com webpack

Passo a passo -

1. Primeiro crie uma pasta e entre nela.
2. Inicie o projeto npm com `npm init -y` - o y significa yes, aceita todos os passos automaticamente
3. Baixe os modulos que vai precisar para o projeto: `npm install @babel/core babel-loader, css-loader, vue, vue-loader, vue-style-loader, vue-template-compiler, webpack` sendo: 
  - "@babel/core": Babel raiz, serve para executar o comando do babel, convertendo para ES2015
  - "babel-loader": Usa o babel com exclusividade para o webpack
  - "css-loader": Usado no webpack para converter os arquivos de css ou vue style
  - "vue": Usado para iniciar o projeto vue
  - "vue-loader": Biblioteca do webpack, para converter arquivos .vue
  - "vue-style-loader": Trabalha em conjunto ao vue-loader, usado no css do .vue
  - "vue-template-compiler": Trabalha em conjunto com o vue-loader, da suporte na conversao .vue
  - "webpack": Modulo que copila o projeto em um unico arquivo.
4. Cria o arquvivo webpack.config.js
5. Crie um arquvivo index.html na raiz =>
```
<html>
  <body>
    <div id="root"></div>
    <script src="static/build.js"></script>
  </body>
</html>
```
6. Crie uma pasta static na raiz
7. Crie uma pasta src para os arquivos na raiz
8. Crie um arquivo main.js dentro de src
9. em main.js escreva:
```
import Vue from 'vue';
import App from './components/App.vue'

new Vue({
  el: '#root',
  render: h => h(App)
})
```
10. Crie uma pasta components dentro de src
11. Dentro de components crie um arquivo App.vue e digite:
```
<template>
  <div>Ola</div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
body {
  margin: 0 auto;
  padding: 0 auto;
}
div {
  background: red
}
</style>
```
12. Agora abra o arquivo package.json e edite em script, acrescentando:
```
"scripts": {
  "build": "webpack"
}
```
13 - Vá ao terminal, entre na raiz do projeto e digite o comando `npm run build`
14 - Abra o arquivo index.html na raiz do projeto.

