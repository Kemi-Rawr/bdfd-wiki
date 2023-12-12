# $blackListUsers
Bloqueia certo usuários de usar o comando. Utiliza nome de usuários ao invés de ID de usuários.

## Sintaxe
```
$blackListUsers[Nome de usuários;...;Mensagem de erro]
```

### Parâmetros
- `Nome de usuários` `(Tipo: String || Indicação: Esvaziável)`: Os nome de usuário(s) para bloquear. Use ponto e vírgulas `;` como um separador para separar múltiplos nome de usuários.
- `Mensagem de erro` `(Tipo: String || Indicação: Esvaziável)`: A mensagem que irá ser enviada quando o nome de usuário do usuário utilizando o comando estiver bloqueado

## Exemplo
```
$nomention
$blackListUsers[kemi_nyah;❌ Você não pode usar este comando!]
Olá $username!
```
![Screenshot_20231210-192852~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/7f6a5fdf-46a7-4221-9946-15ad11af4c94)
