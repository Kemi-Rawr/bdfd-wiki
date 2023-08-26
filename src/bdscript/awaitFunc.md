# $awaitFunc
Usado para iniciar um comando esperado.
## Sintaxe 
```
$awaitFunc[Nome;(ID de Usuário;ID de Canal)]
```

### Parâmetros 
- `Nome` `(Tipo: String || Indicação: Obrigatório)`: O nome usado nas callbacks [`$awaitedCommand[]`](../callbacks/awaitedCommand.md) e [`$awaitedCommandError[]`](../callbacks/awaitedCommandError.md).
  
- `ID de Usuário` `(Tipo: Snowflake || Indicação: Vagável)`: O usuário que o comando esperado irá ser acionado. Usa o autor do comando, se `ID de Usuário` não estiver presente.
  
- `ID de Canal` `(Tipo: Snowflake || Indicação: Opcional)`: O canal onde o comando irá ser esperado. Usa o canal atual, se `ID de Canal` não estiver presente.

## Examplo
```
$nomention
O que você quer que eu fale?
$awaitFunc[falar]
```
![Screenshot_20230825-220212~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/63780938-e1f2-4824-845c-23124765e5ab)
> Para mais informações, veja a [Guia de Comandos Esperados](../guides/general/awaitedCommands.md)
