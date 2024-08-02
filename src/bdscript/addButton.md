# $addButton
Adiciona um botão à uma mensagem

## Sintaxe
```
$addButton[Nova fila?;ID/URL de Interação;Rótulo;Estilo;(Desabilitar?;Emoji;ID de Mensagem)]
```

### Parâmetros
- `Nova fila?` `(Tipo: Bool || Indicação: Obrigatório)`: Se definido como `yes`, o botão vai aparecer em uma nova fila. Se definido como `no`, o botão vai aparecer na mesma fila que o botão anterior.
    > Uma mensagem pode ter no máximo 25 botões (5 filas de 5 botões).
- `ID/URL de Interação` `(Tipo: String, URL || Indicação: Obrigatório)`: Dependendo do tipo do botão, você pode definir como um `ID de Interação` que é então usado na callback `$onInteraction[ID]` ou `URL` se for um botão de link
- `Rótulo` `(Tipo: String || Indicação: Esvaziável)`: O valor de texto visível no botão.
- `Estilo` `(Tipo: Enum || Indicação: Obrigatório)`: É usado para especificar a cor de plano de fundo do botão. Se um botão tem um link/URL, você **tem que** definir o valor como `link`. Veja [essa seção](#button-style) para mais detalhes.
- `Desabilitado?` `(Tipo: Bool || Indicação: Vagável)`: Se definido como `yes`, o botão não pode ser pressionado. Padroniza como `no`.
- `Emoji` `(Tipo: Emoji || Indicação: Vagável)`: Adiciona um emoji dentro do botão. Emojis devem ser colados como *unicode*, *sobrenomes* ou estar no seguinte formato: `<Nome do emoji:ID do emoji>`.
- `ID de Mensagem` `(Tipo: Snowflake || Indicação: Esvaziável)`: Adiciona o botão no ID de Mensagem fornecido. É importante notar que o autor do ID de Mensagem fornecido **tem que** ser o bot.

> Botões interativos não podem ter `IDs` duplicados na mesma mensagem. Então como exemplo, você não pode ter dois botões com o ID definido como `teste`.

> Se `URL` é usado no argumento `ID/URL de Interação`, tem **que começar** com `http://` ou `https://`.

## Estilo do Botão 
Botões podem ter diferentes estilos _(cores de plano de fundo)_.
Aqui, estão todos os valores possíveis para o argumento `style`.
- `primary` - Botão azul
- `secondary` - Botão cinza 
- `success` - Botão verde
- `danger` - Botão vermelho
- `link` - Botão de redirecionamento
![Screenshot_20240801-035007~2](https://github.com/user-attachments/assets/d9ab003c-a9cd-4c06-bde9-e1a751c9a71f)


> Se o estilo `link` é usado, o botão **não vai** mandar nenhuma interação!

## Exemplo
```
$nomention
Oi
$addButton[no;teste;Dizer olá!;primary;no;]
```
![Screenshot_20240801-034148~2](https://github.com/user-attachments/assets/9852da72-d2dc-4636-9fc2-fc101c9059d4)


> Para mais informações, veja a [Guia de Botões](../guides/general/interactions/buttons/aboutButtons.md).
