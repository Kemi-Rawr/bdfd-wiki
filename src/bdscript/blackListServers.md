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
$blackListServers[1096663249346371656;❌ Este comando não pode ser usado aqui!]
**Olá $username!**
*ID da Guilda: $guildID*
```
![Screenshot_20231210-191955~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/748d6b7d-99b3-4fcb-8166-301bcfe83bfd)
![Screenshot_20231210-192019~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/409898ac-cb77-4aa7-be18-34b60c8ba312)
