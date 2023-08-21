# Botões
Nessa seção, você vai aprender como usar o componente botão.

## Conteúdo
[**Funções Usadas**](#funções-usadas) > [**Estilo de Botão**](#estilo-de-botão) > [**Tipo de Botão**](tipo-de-botão) > [**$addButton[]**](#addbutton) > [**$editButton[]**](#editbutton) > [**$removeButtons**](#removebuttons) > [**$removeButtons[]**](#removebuttons-1) > [**$removeComponent[]**](#removecomponent) > [**Criar Interação**](#criar-interação)

## Funções Usadas
- [`$addButton[]`](../../../../bdscript/addButton.md)
- [`$editButton[]`](../../../../bdscript/editButton.md)
- [`$removeButtons`](../../../../bdscript/removeButtons.md)
- [`$removeButtons[]`](../../../../bdscript/removeButtonsComplex.md)
- [`$removeComponent[]`](../../../../bdscript/removeComponent.md)
- [`$onInteraction`](../../../../callbacks/onInteraction.md)
- [`$onInteraction[]`](../../../../callbacks/onInteractionComplex.md)

## Estilo de Botão
- `primary`: Botão azul
- `secondary`: Botão cinza
- `success`: Botão verde
- `danger`: Botão vermelho
- `link`: Botão de redirecionamento

![Screenshot_20230820-162630~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/af2d839c-cc92-40fc-ab13-c082e9795d32)


> Se o estilo `link` é usado, o botão **não enviará** nenhuma interação!

## Tipo de Botão
Tem dois tipos de botões: `interativo` e `link`.

quando um botão interativo é pressionado, ele manda uma interação que pode ser usada junta com `$onInteraction[ID]`.

Todo botão interativo tem um `ID`. Uma `$onInteraction[ID]` callback irá apenas ser acionada quando o botão com o mesmo `ID` é pressionado.
botões interativos podem usar todo estilo exceto `link`.
> Botões links **não enviam** nenhuma interação. Quando é pressionado eles redirecionam o usuário para uma website.
> 
> Botões link **não precisam** setar o valor de seu argumento `style` como `link`.

# $addButton
Adiciona um botão a uma mensagem

## Sintaxe
```
$addButton[Nova fila?;Interação ID/URL;Rótulo;Estilo;(Desabilitar?;Emoji;Mensagem ID)]
```

### Parâmetros
- `Nova fila?` `(Tipo: Bool || Indicação: Obrigatória)`: Se setado como `yes`, o botão vai aparecer em uma nova fila. Se setado como `no`, o botão vai aparecer na mesma fila que o botão anterior.
  > Uma mensagem pode ter no máximo 25 botões (5 filas de 5 botões).

- `Interação ID/URL` `(Tipo: String, URL || Indicação: Obrigatório)`: Dependendo do tipo do botão, você pode setar como `Interaction ID` que é então usada na callback `$onInteraction[ID]` ou `URL` se for um botão de link
  
- `Rótulo` `(Tipo: String || Indicação: Esvaziável)`: O valor de texto visível no botão.
  
- `Estilo` `(Tipo: Enum || Indicação: Obrigatória)`: É usado para especificar a cor de plano de fundo do botão. Se um botão tem um link/URL, você **tem que** setar o valor como `link`. Veja [essa seção](#button-style) para mais detalhes.
  
- `Desabilitar?` `(Tipo: Bool || Indicação: Vagável)`: Se setado como `yes`, O botão não pode ser pressionado. Padroniza como `no`.
  
- `Emoji` `(Tipo: Emoji || Indicação: Vagável)`: Adiciona um emoji dentro do botão. Emojis devem ser colados como *unicode*, *alias* ou estar no seguinte formato: `<nome emoji:emoji ID>`.
  
- `Mensagem ID` `(Tipo: Snowflake || Indicação: Esvaziável)`: Adiciona o botão na mensagem ID fornecida. É importante notar que o autor da mensagem ID fornecida **tem que** ser do bot.

> Botões interativos não podem ter `IDs` duplicados na mesma mensagem. Então como exemplo, você não pode ter dois botões com o ID setado como `teste`.

> Se `URL` é usado no argumento `Interação ID/URL`, tem **que começar** com `http://` ou `https://`.

## Examplo
```
$nomention
Oi
$addButton[no;teste;Dizer olá!;primary;no;]
```
![Screenshot_20230820-161458~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/e4758728-9412-4afb-83f3-70e83a0e84e6)

> Para mais informações, veja a [Guia de Botões](../guides/general/interactions/buttons/aboutButtons.md).

# $editButton
Edita um botão já existente.

## Sintaxe
```
$editButton[Interação ID/URL;Rótulo;Estilo;(Desabilitar?;Emoji;Mensagem ID)]
```

### Parâmetros
- `Interação ID/URL` `(Tipo: String, URL || Indicação: Obrigatório)`: Dependendo do tipo do botão, você pode setar como `Interaction ID` que é então usada na callback `$onInteraction[ID]` ou `URL` se for um botão de link
 
- `Rótulo` `(Tipo: String || Indicação: Esvaziável)`: O valor de texto visível no botão.
  
- `Estilo` `(Tipo: Enum || Indicação: Obrigatória)`: É usado para especificar a cor de plano de fundo do botão. Se um botão tem um link/URL, você **tem que** setar o valor como `link`. Veja [essa seção](#button-style) para mais detalhes.
  
- `Desabilitar?` `(Tipo: Bool || Indicação: Vagável)`: Se setado como `yes`, O botão não pode ser pressionado. Padroniza como `no`.
  
- `Emoji` `(Tipo: Emoji || Indicação: Vagável)`: Adiciona um emoji dentro do botão. Emojis devem ser colados como *unicode*, *alias* ou estar no seguinte formato: `<nome emoji:emoji ID>`. 

- `Mensagem ID` `(Tipo: Snowflake || Indicação: Esvaziável)`: Adiciona o botão na mensagem ID fornecida. É importante notar que o autor da mensagem ID fornecida **tem que** ser do bot.
  
## Examplo
#### Gatilho: `$onInteraction[teste]`
```
$nomention
$username disse olá!
$editButton[teste;Dizer olá!;danger;yes;]
```
![Screenshot_20230820-190047~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/b016d92d-8b61-4f2d-997e-c7cb372ef00c)



# $removeButtons
Remove todos os botões da mensagem acionada.
## Sintaxe
```
$removeButtons
```
## Examplo
#### Gatilho: `$onInteraction[teste]`
```
$nomention
$username removeu todos os botões dessa mensagem!
$removeButtons
```
![Screenshot_20230820-190012~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/e7c10592-390a-47e7-8388-fcf2b389a4c2)



# $removeButtons[]
Remove todos os botões da mensagem especificada.
## Sintaxe
```
$removeButtons[Mensagem ID]
```
### Parâmetros
- `Mensagem ID` `(Tipo: Snowflake || Indicação: Obrigatória)`: Remove botões da mensagem com o ID fornecido. É importante notar que o autor da mensagem fornecida **tem** que ser o bot.
## Examplo
```
$nomention
$username removeu todos os botões da mensagem ID: `$message`
$removeButtons[$message]
```
![Screenshot_20230821-094025~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/c5bab0ce-72da-4243-9d85-202fb78029cc)


# $removeComponent[]
Remove um componente específico de uma mensagem.
## Sintaxe
```
$removeComponent[Interação ID;(Message ID)]
```
> Essa função suporta [Select-menu](../selectMenus/aboutSelectMenu.md) e [Botão](../buttons/aboutButtons.md).
### Parâmetros
- `Interaction ID` `(Type: String || Flag: Required)`: A interação ID do botão para remover da mensagem.
  
- `Message ID` `(Tipo: Snowflake || Indicação: Esvaziável)`: Remove o botão da mensagem com o ID fornecido. É importante notar que o autor da mensagem fornecida **tem** que ser o bot.
## Exemplo
```
$nomention
$username removeu o botão `$message[1]` da mensagem `$message[2]`
$removeComponent[$message[1];$message[2]]
```
![Screenshot_20230821-101946~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/99eaa08e-42e8-42ca-a6f3-c09a2cc3cde3)
![Screenshot_20230821-102020~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/511ed4ca-534f-4aa8-be8a-d395a7acee57)

# Criar interação
### Exemplo com a callback `$onInteraction[]`
1. Crie dois comandos com `!examplo` e `$onInteraction[test]` como gatilhos, respectivamente
2. Cole os seguintes códigos:
   
Código para o comando com o gatilho `!examplo`:
```
$nomention
Pressione o botão abaixo!
$addButton[no;teste;Pressionar;primary]
$addButton[no;botão;Botão desabilitado;secondary;yes]
$addButton[yes;https://botdesignerdiscord.com;Link;link]
```
Código para o comando com o gatilho `$onInteraction[teste]`:
```
$nomention
$editButton[test;Pressionado;primary;yes]
$sendMessage[olá $username!]
```

> Note que a interação ID fornecida em `$onInteraction[]` é a mesma que foi fornecida em `$addButton[]`

> Em `$addButton[]`, `yes` está  sendo usado  no argumento `Nova fila?` para  que o botão então apareça na próxima fila 
3. Execute o comando `!examplo`

![Screenshot_20230821-104622~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/ed0ebd65-25b4-469b-a0f4-e3dafbd13613)
![Screenshot_20230821-104458~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/035d6ff1-87d3-4ec9-8383-543b2b6ab651)

### Exemplo com a callback `$onInteraction`:
1. Crie dois comandos com `!examplo` e `$onInteraction[teste]` como gatilhos, respectivamente
2. Cole os seguintes códigos:

Código para o comando com o gatilho `!examplo`:
```
$nomention
Pressione o botão abaixo!
$addButton[no;teste;Pressionar;primary]
$addButton[no;botão;Botão desabilitado;secondary;yes]
$addButton[yes;https://botdesignerdiscord.com;Link;link]
```
Código para o comando com o gatilho `$onInteraction`:
```
$nomention
$if[$customID==teste]
    $editButton[teste;Pressionado!;primary;yes]
    $sendMessage[olá $username!]
$endif
```
> Note que a interação ID retornada por `$customID` é a mesma que foi fornecida em `$addButton[]`

> Em `$addButton[]`, `yes` está  sendo usado  no argumento `Nova fila?` para  que o botão então apareça na próxima fila

3. Execute o comando `!examplo`


![Screenshot_20230821-105524~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/f7ec3092-9bfc-444f-a1ed-e8524795107f)
![Screenshot_20230821-105621~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/bebcdbd7-b163-46cf-b8ab-4b9a0ea8585a)


> Como [`$onInteraction`](../../../../callbacks/onInteraction.md) e [`$onInteraction[]`](../../../..//callbacks/onInteractionComplex.md) funcionam?

