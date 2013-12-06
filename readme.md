# Workflow de deploy com Grunt
O objetivo desse repositório é mostrar, de uma maneira simples, um workflow para deploy de uma aplicação utilizando o [Grunt](http://gruntjs.com) como ferramenta.
Lembrando que esse repositório tem como objetivo o ensino e não ser um projeto a ser utilizado em produção.

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
Vá ao seu diretório de projetos e crie uma nova pasta. Essa pasta receberá primeiramente, os arquivos de configuração necessários para o Grunt rodar, que são o "package.json" e "Grunt.js".

### Package.json
Nesse arquivo ficaram as configurações do seu projeto. A mais importante delas se refere as suas depêndencias, mas isso falaremos mais adiante. Para criarmos o arquivo, rodamos o comando `npm init` no terminal. Após o comando, digite as informações pedidas. Quando o arquivo for criado, teremos várias instruções nele, mas para o momento, podemos eliminar a maioria das configurações como no exemplo abaixo:

```
{
  "name": "example",
  "version": "0.0.0",
  "description": "an example package.json file"
}
```