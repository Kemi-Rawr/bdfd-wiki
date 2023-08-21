# $addCmdReactions
Adiciona reações a mensagem que acionou o comando.

## Sintaxe
```
$addCmdReactions[Emojis;...]
```

### Parâmetros 
- `Emojis` `(Tipo: Emoji || Indicação: Obrigatório)`: Os emoji(s) com o qual o bot irá reagir. Use ponto e vírgula `;` para separar múltiplos emojis.
> Você pode usar **emojis unicode**, **emoji IDs**, e **emoji aliases**.
> Para **emoji aliases**, Tenha certeza de botar `:` na frente e no fim da alias. 
> Para **emoji IDs**, o bot deve estar presente no servidor que o emoji tem origem.
> 
> Lista de emojis unicode: [😋 Get Emoji](https://getemoji.com) \
> Lista de emojis aliases suportadas: [Emoji Aliases](https://botdesignerdiscord.com/public/emoji_alias_list)

## Examplo
```
$nomention
$addCmdReactions[$message]
```
![Screenshot_20230821-161151~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/9d2f5c18-e250-4123-aab7-9c748b3be614)

### Como conseguir o emoji ID?

> Esse método requer o [Modo Desenvolvedor](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-) ativado!

1. Digite `\:Nome do Emoji:`
2. Envie a mensagem.
3. Copie o ID que retornou. (O emoji ID deve estar nesse formato: `<:nome do emoji:ID>`. Se o emoji for animado, deve estar assim: `<a:nome do emoji:ID>`)
4. Cole o ID em `$addCmdReactions[]`. (Exemplo: `$addCmdReactions[<:chapeu:1143276720779178025>]`)

![ezgif-4-09f0f4237a](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/c1e3cd50-6b8b-41cb-ab96-d7d563280296)


> Se você ainda está tendo problemas, veja a pagina [Solução de Problemas](../resources/troubleshooting.md#the-bot-fails-to-add-reactions) 
