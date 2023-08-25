# $authorOfMessage
Retorna o ID do autor da mensagem fornecida.

## Sintaxe 
```
$authorOfMessage[ID do Canal;ID da Mensagem]
```

### Parâmetros 
- `ID de canal` `(Tipo: Snowflake || Indicação: Obrigatório)`: O canal onde a mensagem está localizada.
  
- `Message ID` `(Type: Snowflake || Flag: Required)`: A mensagem no qual o ID do autor irá ser retornado.

 > [Guia de como pegar o ID de Canal/Mensagem.](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-)

## Examplo
```
$nomention
Autor da mensagem: $username[$authorOfMessage[$channelID;$repliedMessageID]]
```
![Screenshot_20230825-122844~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/b0dc11e2-69fd-4006-be5f-83851a9d85fe)


