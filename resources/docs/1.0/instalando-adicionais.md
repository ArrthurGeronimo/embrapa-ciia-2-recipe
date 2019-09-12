# Instalando Adicionais

---

- [AdminLTE 3](#adminlte)
- [Font Awesome](#font-awesome)
- [Vue Router](#vue-router)
- [Vue Progress](#vue-progress)
- [Sweet Alert](#sweet-alert)

<a name="adminlte"></a>
## AdminLTE 3

Para o layout geral foi utilizado o `AdminLTE 3`. Trata-se de um template completo de administração criado a partir do `Bootstrap 4`. No caso utilizaremos somente seus estilos `CSS` , suas estruturas `HTML` e seus scripts em `JavaScript` para deixar a interface bonita e responsiva. </br>

#### Links Úteis
- Para consultar o site oficial clique [aqui](https://adminlte.io/). </br>
- Para consultar as versões de lançamento clique [aqui](https://github.com/almasaeed2010/AdminLTE/releases). </br>
- Para consultar a demo da versão utilizada no sistema clique [aqui](https://adminlte.io/themes/dev/AdminLTE/index.html). </br>
</br>

#### Instalação
> {warning} Na data dessa documentação foi utilizada a versão `AdminLTE 3 Alpha-2`, podendo ter saído de sua fase alfa na data atual.


Para instalar o template, basta digitar o seguinte comando no CMD/Terminal:
<larecipe-card shadow>
    npm install admin-lte@v3.0.0-alpha.2 --save
</larecipe-card>
</br>

##### Integração
Para usá-lo em nossa aplicação, precisamos copilar o seus arquivos CSS e JS. Para isso, bastar abrir o arquivo `bootstrap.js` localizado no caminho `resources->assets->js` e colocar o código:
```php
	//AdminLTE
	require('admin-lte');
```
Depois abrir o arquivo `app.scss` localizado no caminho `resources->assets->sass` e colocar o código:
```php
	//AdminLTE
	@import '-admin-lte/dist/css/adminlte.css';
```

<a name="font-awesome"></a>
## Font Awesome
Para a utilização de ícones foi utilizado o framework `Font Awesome`. Para acessar o site ofical clique [aqui](https://fontawesome.com/). </br>
</br>

##### Instalação
Para instalar basta executar o comando:
<larecipe-card shadow>
    npm install --save-dev @fortawesome/fontawesome-free
</larecipe-card>
</br>

##### Integração
Para usar na aplicação basta abrir o arquivo `app.scss` localizado no caminho `resources->assets->sass` e colocar o código:
```php
	//Font Awesome
	$fa-font-path:"../webfonts";
	@import "~@fortawesome/fontawesome-free/scss/fontawesome.scss";
	@import "~@fortawesome/fontawesome-free/scss/solid.scss";
	@import "~@fortawesome/fontawesome-free/scss/brands.scss";
```


<a name="vue-router"></a>
## Vue Router

O Vue Router é o plugin de administração de rotas oficial do Vue.js. Ele se integra profundamente ao núcleo do Vue.js para facilitar a construção de aplicativos de página única.
</br>

##### Instalação
Para instalar basta executar o comando:
<larecipe-card shadow>
    npm install vue-router --save
</larecipe-card>
</br>

##### Integração
Para utilizar o plugin é preciso chamá-lo dentro do layout Master do sistema, para isso, basta ir até o arquivo de layout e na seção do `Main Content` e chamar o componente das rotas, como no exemplo abaixo:
```html
	<!-- Main content -->
	<div class="content">
		<div class="container-fluid">
			<router-view></router-view>
		</div>
	</div>
	<!-- /Main content -->

```
</br>
Mas antes é preciso `importá-lo` para nossa aplicação, para isso, basta abrir o arquivo `app.js` localizado no caminho `resources->assets->js->components` da nossa aplicação e digitar o código abaixo:
```js
	//Vue Router
	import VueRouter from 'vue-router';
	Vue.use(VueRouter);

```
</br>
Para adicionar rotas ao Vue.js é preciso adicioná-las a varíavel `routes`, assim como seus respectivos componentes, como no exemplo abaixo:
```js
	//Routes
	const routes = [
		{ path: '/dashboard', component: required('./components/Dashboard.vue') },
		{ path: '/profile', component: required('./components/Profile.vue') }
	]

```
</br>
Agora será preciso criar uma instância dessa nova rota, segue o código abaixo para essa tarefa:
```js
	//New Router
	const router = new VueRouter({
		routes // short for 'routes: routes'
	})

```
</br>
E por fim adicioná-lo a nossa aplicação Vue.js, como no exemplo abaixo:
```js
	//App
	const app = new Vue({
		el: '#app',
		router
	});

```
</br>
> {warning} Não se usa mais a tag `a` do HTML para links, agora se usa a tag `router-link` do Vue.js. Segue a nova sintaxe: `<router-link to="/dashboard"></router-link>`

</br>

##### Melhorando a U.X.
Para que as rotas funcionem de maneira a não entrar em conflito com nosso back-end, usaremos o `mode: 'history'` do `Vue-Routes`. Basta ir até o arquivo pai da nossa aplicação, no caso o `app.js` localizado no caminho `resources->assets->js->components` e no passo para criar uma nova instância de rotas colocar o seguinte comando:
```js
	//New Router
	const router = new VueRouter({
		mode: 'history',
		routes // short for 'routes: routes'
	})

```
Feito isso é só informar ao Laravel o que fazer caso digite uma rota na barra de navegação que ele não saiba o destino. Abra o arquivo `web.php` localizado dentro da pasta `routes` e digitar o seguinte comando:
```php
Route::get('{path}', "HomeController@index")->where('path', '([A-z\d-\/_.]+)?');
```

<a name="vue-progress"></a>
## Vue Progress

<a name="sweet-alert"></a>
## Sweet Alert