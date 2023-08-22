# $addMessageReactions
Adiciona reações na mensagem especificada.

## Sintaxe
```
$addMessageReactions[Canal ID;Mensagem ID;Emojis;...]
```

### Parameters
- `Canal ID` `(Tipo: Snowflake || Indicação: Obrigatório)`: O ID do canal onde a mensagem está localizada.
- `Mensagem ID` `(Tipo: Snowflake || Indicação: Obrigatório)`: O ID da mensagem no qual as reações irão ser adicionadas.
- `Emojis` `(Type: Emoji || Flag: Required)`: Os emoji(s) para adicionar como reações na mensagem. Use ponto e vírgula `;` como um separador para separar múltiplos emojis.

> Você pode usar **emojis unicode**, **emoji IDs**, e **emoji aliases**.
> > Para **emoji aliases**, tenha certeza de colocar `:` na frente e no fim da alias.
> > Para **emoji IDs**, O bot deve estar presente no servidor que o emoji tem origem.
> 
> Lista de emojis unicode: [😋 Get Emoji](https://getemoji.com) \
> Lista de emoji aliases suportado: [Emoji Aliases](https://botdesignerdiscord.com/public/emoji_alias_list)

## Examplo
```
$nomention
$addMessageReactions[$channelID;$repliedMessageID;✨;:snowflake:;<:clueless:1023577032287846510>]

Reações adicionadas na mensagem com sucesso!
```
![ezgif-1-28cb3aa457](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/35ead963-a6f8-4278-a966-52b25486816b)


## How to get emoji ID?

> This method requires [Developer Mode](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-) to be enabled! 

1. Type `\:TheEmojiName:`
2. Send the message.
3. Copy the ID it returns. (The emoji ID should be in this format: `<:emojiName:ID>`. If the emoji is animated, it should look like this: `<a:emojiName:ID>`)
4. Input the emoji ID into `$addMessageReactions[]`. (e.g. `$addMessageReactions[$channelID;1123254137547653222;<:hollyDab:828628880629825546>]`)

![example2](https://media.discordapp.net/attachments/609162277312266280/745309789491298415/My_Movie_0.gif)

> If you're still having issues, check the [Troubleshooting](../resources/troubleshooting.md#the-bot-fails-to-add-reactions) page.
