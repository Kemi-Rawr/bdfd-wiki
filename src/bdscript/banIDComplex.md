# $banID[]
Bane o usuário usando seu ID.

## Sintaxe
```
$banID[Motivo;(ID do Usuário)]
```

### Parâmetros
- `Motivo` `(Tipo: String || Indicação: Esvaziável)`: O motivo para o banimento, que vai ser salvo no registro de auditoria.
   > Use [`$getBanReason[]`](./getBanReason.md) para pegar o motivo do banimento.
- `ID do Usuário` `(Tipo: Snowflake || Indicação: Vagável)`: O usuário para banir. Se vazio, o ID irá ser pego da última parte da mensagem do autor
## Exemplo
```
$nomention
$onlyAdmin[Você precisa da permissão `admin` para usar esse comando!]
$argsCheck[>1;Por favor forneça um `usuário`. Sintaxe: `!banir (usuário) <motivo>`]
$onlyIf[$findUser[$message[1];no]!=;Falha ao encontrar o usuário!]
<@$findUser[$message[1];no]> foi banido!
$banID[$replaceText[$message;$message[1];;1];$findUser[$message[1];no]]
```
![Screenshot_20231210-183547~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/191462de-3a15-419f-b34e-2d1aaaa9edc4)
![Screenshot_20231210-183611~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/a23f7182-0af1-462a-ae25-f42acbdfd38e)

