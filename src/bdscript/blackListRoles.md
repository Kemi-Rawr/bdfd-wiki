# $blackListRoles
Bloqueia usuários com certos cargo(s) de usar o comando. Se o usuário possuir qualquer cargo na lista negra, eles não poderão usar o comando. Usa Nomes de Cargos ao invés de IDs de Cargos

## Syntax
```
$blackListRoles[Nomes de Cargos;...;Mensagem de Erro]
```

### Parameters
- `Nomes de Cargos` `(Tipo: String || Indicação: Esvaziável)`: Os nome(s) dos cargo(s) para bloquear. Use ponto e vírgulas `;` como um separador para separar multiplos nomes de cargos.
- `Mensagem de Erro` `(Tipo: String || Indicação: Esvaziável)`: A mensagem que irá ser enviada se o usuário possuir um cargo da lista negra.

## Example
```
$nomention
$blackListRoles[Dono;Bot;❌ Você não pode usar este comando!]
Pong! $ping ms
```
![Screenshot_20231210-185743~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/550d8edf-c402-4f60-831c-1820c82e39a0)

