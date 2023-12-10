# $blackListServers
Bloqueia certos servidores de usar o comando.

## Sintaxe 
```
$blackListServers[IDs de Guildas;...;Mensagem de Erro]
```

### Parâmetros
- `IDs de Guildas` `(Tipo: Snowflake || Indicação: Esvaziável)`: Os servidor(es) para bloquear de usar o comando. Use ponto e vírgulas `;` como um separador para separar múltiplos IDs de Servidores.
   > [Como eu acho IDs de servidores? (me clique)](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-)
- `Mensagem de Erro` `(Tipo: String || Indicação: Esvaziável)`: A mensagem que irá ser enviada se o comando for usado em um servidor bloqueado.


## Exemplo
```
$nomention
$blackListServers[1009018669982031912;❌ Este comando não pode ser usado aqui!]
**Olá $username!**
*ID da Guilda: $guildID*
```
![example](https://user-images.githubusercontent.com/113303649/211995843-0d9eba33-e36a-484f-ad97-eb6e67391af1.png)\
![example](https://user-images.githubusercontent.com/113303649/211996168-47ba94ff-e03d-40f9-8b33-5758454f5ce9.png)
