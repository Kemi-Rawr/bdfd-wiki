# $addCmdReactions
Adiciona reações a mensagem que acionou o comando.

## Sintaxe
```
$addCmdReactions[Emojis;...]
```

### Parâmetros 
- `Emojis` `(Tipo: Emoji || Indicação: Obrigatório)`: Os emoji(s) com o qual o bot irá reagir. Use ponto e vírgula `;` para separar múltiplos emojis.
> Você pode usar **emojis unicode**, **IDs de emojis**, e **sobrenomes de emoji**.
> 
> > Para **sobrenomes de emoji**, certifique-se de botar `:` na frente e no fim do sobrenome.
> >
> > Para **IDs de emojis**, o bot deve estar presente no servidor que o emoji tem origem.
> 
> Lista de emojis unicode: [😋 Get Emoji](https://getemoji.com) \
> Lista de sobrenomes de emojis suportados: [Emoji Aliases](https://botdesignerdiscord.com/public/emoji_alias_list)

## Examplo
```
$nomention
$addCmdReactions[$message]
```
![Screenshot_20240801-035722~2](https://github.com/user-attachments/assets/9b9ebbf4-f984-4ecb-80ba-378008f47ba2)


### Como conseguir o emoji ID?

> Esse método requer o [Modo Desenvolvedor](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-) ativado!

1. Digite `\:Nome do Emoji:`
2. Envie a mensagem.
3. Copie o ID que retornou. (O emoji ID deve estar nesse formato: `<:nome do emoji:ID>`. Se o emoji for animado, deve estar assim: `<a:nome do emoji:ID>`)
4. Cole o ID em `$addCmdReactions[]`. (Exemplo: `$addCmdReactions[<:clueless:1268464129069416449>]`)
![ezgif-7-963b6c6717](https://github.com/user-attachments/assets/a07916b5-48d8-40b4-adc1-b7b1d185884b)



> Se você ainda está tendo problemas, veja a pagina [Solução de Problemas](../resources/troubleshooting.md#the-bot-fails-to-add-reactions) 
