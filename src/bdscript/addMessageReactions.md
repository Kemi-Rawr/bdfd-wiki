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


## Como conseguir o emoji ID?

> Esse método requer o [Modo Desenvolvedor](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-) ativado!

1. Digite `\:Nome do Emoji:`
2. Envie a mensagem.
3. Copie o ID que retornou. (O emoji ID deve estar nesse formato: `<:nome do emoji:ID>`. Se o emoji for animado, deve estar assim: `<a:nome do emoji:ID>`)
4. Cole o ID em `$addMessageReactions[]`. (Exemplo: `$addMessageReactions[...;...;<:chapeu:1143276720779178025>]`)

![ezgif-4-09f0f4237a](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/c1e3cd50-6b8b-41cb-ab96-d7d563280296)


> Se você ainda está tendo problemas, veja a pagina [Solução de Problemas](../resources/troubleshooting.md#the-bot-fails-to-add-reactions) 
