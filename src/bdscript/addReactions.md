# $addReactions
Adiciona reações a resposta do bot.

## Sintaxe
```
$addReactions[Emojis;...]
```

### Parâmetros 
- `Emojis` `(Tipi: Emoji || Indicação: Obrigatório)`: Os emoji(s) com o qual o bot irá reagir. Use ponto e vírgula `;` para separar múltiplos emojis.

> Você pode usar **emojis unicode**, **emoji IDs**, e **emoji aliases**.
> 
> > Para **emoji aliases**, Tenha certeza de botar `:` na frente e no fim da alias.
> >
> > Para **emoji IDs**, o bot deve estar presente no servidor que o emoji tem origem.
> 
> Lista de emojis unicode: [😋 Get Emoji](https://getemoji.com) \
> Lista de emojis aliases suportadas: [Emoji Aliases](https://botdesignerdiscord.com/public/emoji_alias_list)
## Examplo
```
$nomention
Escolha um número!
$addReactions[1️⃣;:two:;3️⃣]
```
![Screenshot_20230821-230948~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/952bb873-04ef-4dc3-aab2-c72f38ed1fd9)

### How to get emoji ID?

> This method requires [Developer Mode](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-) to be enabled! 

1. Type `\:TheEmojiName:`
2. Send the message.
3. Copy the ID it returns. (The emoji ID should be in this format: `<:emojiName:ID>`. If the emoji is animated, it should look like this: `<a:emojiName:ID>`)
4. Input the emoji ID into `$addReactions[]`. (e.g. `$addReactions[<:hollyDab:828628880629825546>]`)

![example](https://media.discordapp.net/attachments/609162277312266280/745309789491298415/My_Movie_0.gif)

> If you're still having issues, check the [Troubleshooting](../resources/troubleshooting.md#the-bot-fails-to-add-reactions) page.
