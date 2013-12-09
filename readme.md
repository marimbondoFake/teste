# Workflow de deploy com Grunt
O objetivo desse repositório é mostrar, de uma maneira simples, um workflow para deploy de uma aplicação utilizando o [Grunt](http://gruntjs.com) como ferramenta.
Lembrando que esse repositório tem como objetivo o ensino e não é um projeto para ser utilizado em produção. Aproveite as dicas e faça o seu próprio Gruntfile :)

## Tarefas executadas
*

## Instalações básicas

- Ter o [nodeJS](http://nodejs.org) disponível no seu ambiente;
- Algum Terminal (para usuários OSX recomendo o [iTerm2](http://www.iterm2.com/));

### Instalando o Grunt
- No terminal rodar o comando:

`npm install -g grunt-cli`

Dessa maneira, teremos o Grunt instalado de maneira global para usarmos em qualquer um dos nossos projetos.
Para mais informações, visite o [guia oficial](http://gruntjs.com/getting-started).

## Configurando um novo projeto
Vá ao seu diretório de projetos e crie uma nova pasta. Essa pasta receberá, primeiramente, os arquivos de configuração necessários para o Grunt rodar, que são o `package.json` e `Gruntfile.js.

### Package.json
Nesse arquivo ficaram as configurações do seu projeto. A mais importante delas se refere as suas depêndencias, mas isso falaremos mais adiante. Para criarmos o arquivo, rodamos o comando `npm init` no terminal. Após o comando, digite as informações pedidas. Quando o arquivo for criado, teremos várias instruções nele, mas para o momento, podemos eliminar a maioria das configurações e deixa-lo como no exemplo abaixo:

```
{
  "name" : "example",
  "version" : "0.0.0",
  "description" : "an example package.json file"
}
```
Agora instalaremos o Grunt propriamente dito. Utilizaremos o comando:
`npm install grunt --save-dev`

Aqui é importante entender a instrução `--save-dev`. Sempre que instalarmos um plugin com ela, a chamada do plugin será inscrita no nosso package.json. Dessa maneira, ele ficará assim:
```
{
  "name" : "example",
  "version" : "0.0.0",
  "description" : "an example package.json file",
  "devDependencies" : {
    "grunt" : "~0.4.2"
  }
}
```

A vantagem disso é que podemos utilizar o mesmo `package.json` em qualquer outro projeto, juntamente com as suas dependências. Ao criarmos um novo projeto, copiamos esse mesmo `package.json` e utilizamos o comando `npm install`. Dessa maneira, todos os nossos plugins serão instalados automaticamente, sem a necessidade de instalarmos "um por um".

### Gruntfile.js
Todas as chamadas e comportamentos dos módulos vão ser editadas nesse arquivo.
Como estamos aprendendo a utilizar o Grunt, não faremos [scaffolding](http://gruntjs.com/project-scaffolding) de algum projeto, vamos fazer o arquivo na mão mesmo.
Primeiro, criamos o arquivo `Gruntfile.js com as seguintes instruções:
```
module.exports = function(grunt) {

	'use strict';

	grunt.initConfig({

	});

	grunt.registerTask('default', []);

};
``
Explicando:
- `grunt.initConfig({})` é onde as instruções para nossos plugins vão ficar. Ou seja, as configurações necessárias para o funcionamento de acordo com nossas configurações desejadas.
- `grunt.registerTask('default', [])` aqui ficaram as chamadas das nossas tarefas. Ela será definidada por um nome, aqui representado por 'default' e quais tarefas serão executadas, representados através de um Array.
