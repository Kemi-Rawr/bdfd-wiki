# $addButton
Adiciona um botão à uma mensagem

## Sintaxe
```
$addButton[Nova fila?;ID/URL de Interação;Rótulo;Estilo;(Desabilitar?;Emoji;ID de Mensagem)]
```

### Parâmetros
- `Nova fila?` `(Tipo: Bool || Indicação: Obrigatório)`: Se setado como `yes`, o botão vai aparecer em uma nova fila. Se setado como `no`, o botão vai aparecer na mesma fila que o botão anterior.
    > Uma mensagem pode ter no máximo 25 botões (5 filas de 5 botões).
- `ID/URL de Interação` `(Tipo: String, URL || Indicação: Obrigatório)`: Dependendo do tipo do botão, você pode setar como um `ID de Interação` que é então usado na callback `$onInteraction[ID]` ou `URL` se for um botão de link
- `Rótulo` `(Tipo: String || Indicação: Esvaziável)`: O valor de texto visível no botão.
- `Estilo` `(Tipo: Enum || Indicação: Obrigatório)`: É usado para especificar a cor de plano de fundo do botão. Se um botão tem um link/URL, você **tem que** setar o valor como `link`. Veja [essa seção](#button-style) para mais detalhes.
- `Desabilitado?` `(Tipo: Bool || Indicação: Vagável)`: Se setado como `yes`, o botão não pode ser pressionado. Padroniza como `no`.
- `Emoji` `(Tipo: Emoji || Indicação: Vagável)`: Adiciona um emoji dentro do botão. Emojis devem ser colados como *unicode*, *alias* ou estar no seguinte formato: `<nome do emoji:ID do emoji>`.
- `ID de Mensagem` `(Tipo: Snowflake || Indicação: Esvaziável)`: Adiciona o botão no ID de Mensagem fornecido. É importante notar que o autor do ID de Mensagem fornecido **tem que** ser o bot.

> Botões interativos não podem ter `IDs` duplicados na mesma mensagem. Então como exemplo, você não pode ter dois botões com o ID setado como `teste`.

> Se `URL` é usado no argumento `ID/URL de Interação`, tem **que começar** com `http://` ou `https://`.

## Estilo do Botão 
Botões podem ter diferentes estilos _(cores de plano de fundo)_.
Aqui, estão todos os valores possíveis para o argumento `style`.
- `primary` - Botão azul
- `secondary` - Botão cinza 
- `success` - Botão verde
- `danger` - Botão vermelho
- `link` - Botão de redirecionamento
![Screenshot_20230820-162630~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/29119e57-1c58-4dfe-abe8-0dd64949f8c8)

> Se o estilo `link` é usado, o botão **não vai** mandar nenhuma interação!

## Exemplo
```
$nomention
Oi
$addButton[no;teste;Dizer olá!;primary;no;]
```
![Screenshot_20230820-161458~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/e4758728-9412-4afb-83f3-70e83a0e84e6)

> Para mais informações, veja a [Guia de Botões](../guides/general/interactions/buttons/aboutButtons.md).
