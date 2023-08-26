# $awaitFunc
Usado para iniciar um comando esperado.
## Sintaxe 
```
$awaitFunc[Nome;(ID de Usuário;ID de Canal)]
```

### Parâmetros 
- `Nome` `(Tipo: String || Indicação: Obrigatório)`: O nome usado nas callbacks [`$awaitedCommand[]`](../callbacks/awaitedCommand.md) e [`$awaitedCommandError[]`](../callbacks/awaitedCommandError.md).
  
- `ID de usuário` `(Tipo: Snowflake || Indicação: Vagável)`: O usuário que o comando esperado irá ser acionado. Usa o autor do comando, se `ID de usuário` não estiver presente.
  
- `ID de Canal` `(Tipo: Snowflake || Indicação: Opcional)`: O canal onde o comando irá ser esperado. Usa o canal atual, se `ID de Canal` não estiver presente.

## Examplo
```
$nomention
O que você quer que eu fale?
$awaitFunc[say]
```
