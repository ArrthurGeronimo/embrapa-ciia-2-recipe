# Possíveis erros do Laravel

---

- [Max Key Length](#max-key-length)
- [CSRF token not found](#csrf-token-not-found)

<a name="max-key-length"></a>
## 1071 Specified key was too long

Bem comum do Laravel, porém não é bem um erro e sim um opção de segurança do framework. Quando se cria um projeto Laravel onde você irá usar comandos de `migrate` para gerar tabelas no banco de dados, você irá se deparar com a seguinte mensagem de erro, `Syntax error or access violation: 1071 Specified key was too long; max key lenght is 1000 bytes`. Para corrigir, basta ir até o arquivo `AppServiceProvider.php` localizado no caminho `app->Providers` e na função boot escrever conforme abaixo:
```php
use Illuminate\Support\Facades\Schema;

public function boot()
{
	Schema::defaultStringLenght(191);
}
```
</br>

<a name="csrf-token-not-found"></a>
## CSRF token not found

Para corrigir esse problema basta adicionar o código abaixo na sua tag HTML `<head>` do layout principal:
```html
	<!-- CSRF Token -->
	<meta>
```
