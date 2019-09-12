# Visão Geral

---

- [O Sistema](#o-sistema)
- [Back-End](#back-end)
- [Front-End](#front-end)
- [Adicionais](#adicionais)

<a name="o-sistema"></a>
## O Sistema
Para o desenvolvimento do sistema foi planejado a utilização da `Arquitetura MVC`, que possibilita a divisão do projeto em camadas muito bem definidas, onde cada uma delas, o Model, o Controller e a View, executam somente o que lhe é definido e nada mais do que isso. Para o controle de requisições foi adotada a utilização do modelo `RESTful`, onde o sistema possui a capacitade de aplicar os princípios de `REST`.

<a name="back-end"></a>
## Back-End
Para o desenvolvimento do back-end foi escolhido o framework `Laravel` na sua versão 5.7. O Laravel é um framework de desenvolvimento rápido para PHP, livre e de código aberto, cujo o principal objetivo é permitir ao programador trabalhar de forma estruturada e rápida. O Laravel utiliza o `Composer` para gerenciar suas dependências, algo que praticamente toda aplicação PHP moderna faz, porém no nosso sistema em questão, além do Composer, utilizaremos o `NPM` também para gerenciar algumas dependências. O Laravel possui uma excelente documentação no seu site.
> {primary} Para maiores informações sobre o Laravel, consulte a seção sobre o mesmo no sumário da documentação do projeto.


<a name="front-end"></a>
## Front-End
Para o desenvolvimento do front-end foi escolhido o framework `Vue.js` (pronuncia-se view, em inglês). Trata-se de um framework progressivo para a construção de interfaces de usuário e ao contrário de outros frameworks monolíticos, o Vue foi projetado desde sua concepção para ser adotável incrementalmente. A biblioteca principal é focada exclusivamente na camada visual (view layer), sendo fácil adotar e integrar com outras bibliotecas ou projetos existentes. Por outro lado, o Vue também é perfeitamente capaz de dar poder a sofisticadas Single-Page Applications quando usado em conjunto com ferramentas modernas e bibliotecas de apoio. É um framework que utiliza a lingagem `JavaScript`.
> {primary} Para maiores informações sobre o Vue.js, consulte a seção sobre o mesmo no sumário da documentação do projeto.

<a name="adicionais"></a>
## Adicionais
No sistema também foram adotadas diversos adicionais visando um bom e moderno funcionamento. </br>
Para o template geral foi escolhido como base o template `AdminLTE 3` </br>
Para tornar o sistema responsivo e visual bonito foi utilizado o `Bootstrap 4` </br>
Para administrar as rotas com os componentes do Vue.js foi utilizado o `Vue Router` </br>