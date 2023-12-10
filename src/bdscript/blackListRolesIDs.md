# $blackListRolesIDs
Bloqueia usuários com certos cargos de usar o comando. Se o usuário possuir qualquer cargo da lista negra, eles não poderão usar o comando.

## Syntax
```
$blackListRolesIDs[IDs de Cargos;...;Mensagem de Erro]
```

### Parameters
- `IDs de Cargos` `(Tipo: Snowflake || Indicação: Esvaziável)`: Os cargo(s) que serão bloqueados. Use ponto e vírgulas `;` como um separador para separar múltiplos IDs de Cargos.
- `Mensagem de Erro` `(Tipo: String || Indicação: Esvaziável)`: A mensagem que irá ser enviada se o usuário possuir um cargo da lista negra.

## Exemplo
```
$nomention
$blackListRolesIDs[1009019299987476540;1014547313957539901;❌ Você não pode usar este comando!]
Pong! $ping ms
```
![Screenshot_20231210-190458~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/341b794b-f632-4a97-9a76-2090aea4c0da)

