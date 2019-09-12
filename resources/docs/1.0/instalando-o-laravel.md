# Instalando o Laravel

---

- [Requisitos](#requisitos)
- [Instalando o Laravel](#instalando-o-laravel)
- [Instalando Dependências](#instalando-dependencias)

> {info} Todos os passos descritos aqui na documentação estão na `documentação original` do Laravel, que pode ser acessada clicando [aqui](https://laravel.com/docs/5.7).

<a name="requisitos"></a>
## Requisitos

A estrutura do Laravel possui alguns requisitos de sistema, será necessário garantir que seu servidor atenda aos seguintes requisitos:
- PHP >= 7.1.3
- Extensão PHP OpenSSL
- Extensão PHP PDO
- Extensão PHP Mbstring
- Extensão PHP Tokenizer
- Extensão PHP XML
- Extensão PHP Ctype
- Extensão PHP JSON
- Extensão PHP BCMath

<a name="instalando-o-laravel"></a>
## Instalando o Laravel
> {danger} O Laravel utiliza o Composer para gerenciar suas dependências. Então, antes de usar o Laravel, certifique-se de ter o `Composer` instalado em sua máquina.


Navegue através do CMD/Terminal (depende do seu sistema operacional) até a pasta onde o projeto será instalado e coloque o seguindo comando:
<larecipe-card shadow>
    composer create-project --prefer-dist laravel/laravel NOME_PROJETO
</larecipe-card>
Aguarde a instalação, caso ocorra tudo bem o projeto será criado com sucesso. </br>
Para fazer o teste basta criar o servidor e testar em qualquer navegador. Para criar o servidor você precisa entrar na pasta através do CMD/Terminal onde o projeto foi criado e digitar o seguindo comando:
<larecipe-card shadow>
	php artisan serve
</larecipe-card>
O Sistema poderá ser visto no endereço `http://localhost:8000:`
> {warning} Não esqueça de colocar as informações referentes ao Banco de Dados no arquivo `.env`

<a name="instalando-dependencias"></a>
## Instalando Dependências
Para garantir o funcionamento do sistema de forma precisa é preciso instalar suas dependências básicas, incluindo o `Vue.js`. Para isso basta digitar o seguinte comando:
<larecipe-card shadow>
	npm install
</larecipe-card>
Esse processo costuma levar um bom tempo, dependendo da velocidade da internet.