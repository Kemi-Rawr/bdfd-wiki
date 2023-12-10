# $blackListIDs
Bloqueia certo usuários de usar o comando.

## Sintaxe
```
$blackListIDs[IDs de Usuários;...;Mensagem de Erro]
```

### Parâmetros
- `IDs de Usuários` `(Tipo: Snowflake || Indicação: Esvaziável)`: Os usuário(s) para bloquear de usar o comando. Use ponto e vírgulas `;` como um separador para separar multiplos IDs de Usuários.
  > [Como obter um ID de Usuário?](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-)
- `Mensagem de Erro` `(Tipo: String || Indicação: Esvaziável)`: A mensagem que irá ser enviada quando o usuário que usou o comando estiver bloqueado.

## Exemplo
```
$nomention
$blackListIDs[1043373475747864647;527611538291425321;❌ Você não pode usar este comando!]
Pong! $ping ms
```
