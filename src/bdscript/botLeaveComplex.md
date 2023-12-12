# $botLeave[]
Força o bot a sair do servidor que corresponde ao [ID do servidor](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID) fornecido.

## Sintaxe
```
$botLeave[ID da Guilda]
````

### Parâmetros 
- `ID da Guilda` `(Tipo: Snowflake || Indicação: Obrigatório)`: O ID da guilda para sair.

## Exemplo
```
$nomention
$sendMessage[Eu sai do servidor: `$serverName[$message]`.]
$botLeave[$message]
```
![Screenshot_20231212-033942~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/d3d90acc-c7fd-4488-95d4-7fba9e416864)

> If you are using **BDScript 2**, put `$botLeave[]` at the very bottom of the code so that the code works correctly i.e:
> 
> ❌ Not correct:
> ```
> $botLeave[$message]
> $nomention
> $sendMessage[I left this server!]
> ```
>
> ✅ Correct:
> ```
> $nomention
> $sendMessage[I left this server!]
> $botLeave[$message]
> ```
