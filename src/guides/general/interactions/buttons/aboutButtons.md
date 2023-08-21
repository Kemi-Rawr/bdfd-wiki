# Botões
Nessa seção, você vai aprender como usar o componente botão.

## Conteúdo
[**Funções Usadas**](#funções-usadas) > [**Estilo de Botão**](#estilo-de-botão) > [**Tipo de Botão**](tipo-de-botão) > [**$addButton[]**](#addbutton) > [**$editButton[]**](#editbutton) > [**$removeButtons**](#removebuttons) > [**$removeButtons[]**](#removebuttons-1) > [**$removeComponent[]**](#removecomponent) > [**Criar Interação**](#create-interaction)

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


> Se o estilo `link` é usado, o botão **não enviará** uma interação!

## Tipo de Botão
Tem dois tipos de botões: `interativo` e `link`.

quando um botão interativo é pressionado, ele manda uma interação que pode ser usada junta com `$onInteraction[ID]`.

Todo botão interativo tem um `ID`. Uma `$onInteraction[ID]` callback irá apenas ser acionada quando o botão com o mesmo `ID` é pressionado.
botões interativos podem usar todo estilo exceto `link`.
> Link buttons **don't send** any interactions. When they're pressed they forward the user to a website.
> 
> Link buttons **need to** set their `style` argument value to `link`.

# $addButton
Adiciona um botão à uma mensagem

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
- `Desabilitar?` `(Tipo: Bool || Indicação: Vagável)`: Se setado como `yes`, O botão não pode ser pressionado. Padroniza como `no`. _(Opcional)_
- `Emoji` `(Tipo: Emoji || Indicação: Vagável)`: Adiciona um emoji dentro do botão. Emojis devem ser colados como *unicode*, *alias* ou estar no seguinte formato: `<nome emoji:emoji ID>`. _(Opcional)_

- `Mensagem ID` `(Tipo: Snowflake || Indicação: Esvaziável)`: Adiciona o botão na mensagem ID fornecida. É importante notar que o autor da mensagem ID fornecida **tem que** ser do bot. _(Opcional)_
## Example
#### Trigger: `$onInteraction[teste]`
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
#### Trigger: `$onInteraction[teste]`
```
$nomention
$username removeu todos os botões dessa mensagem!
$removeButtons
```
![Screenshot_20230820-190012~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/38ea29d7-08a4-48ad-b96c-721d8ae90b59)


# $removeButtons[]
Remove todos os botões da mensagem específicada.
## Sintaxe
```
$removeButtons[Mensagem ID]
```
### Parâmetros
- `Mensagem ID` `(Tipo: Snowflake || Indicação: Obrigatória)`: Removes buttons from the message with the provided ID. It's important to note that provided message ID author **has to** be the bot.
## Example
```
$nomention
$username removed all buttons from the specified message id
$removeButtons[$message]
```
![example](https://user-images.githubusercontent.com/113303649/210875885-aa20517e-1c37-4206-8eee-eefa765eb40a.png)

# $removeComponent
Removes a certain component from a message.
## Syntax
```
$removeComponent[interaction ID;(message ID)]
```
> This function supports [select-menu](../selectMenus/aboutSelectMenu.md) and [button](../buttons/aboutButtons.md).
### Parameters
- `interaction ID` `(Type: String || Flag: Required)`: The interaction ID of the button, to remove from the message. 
- `message ID` `(Type: Snowflake || Flag: Vacantable)`: Removes the button from the message with the provided ID. It's important to note that provided message ID author **has to** be the bot. _(Optional)_
## Example
```
$nomention
$username successfully removed the button!
$removeComponent[test;$message]
```
![example](https://user-images.githubusercontent.com/113303649/211163378-2aaa540d-b0a1-4511-8f34-6a91260b079d.png)

![example](https://user-images.githubusercontent.com/113303649/211163615-ecffddcf-1d2b-4065-8445-9ec7ed1eb2b4.png)

# Create interaction
### Example with `$onInteraction[]` callback:
1. Create two commands with `!example` and `$onInteraction[test]` triggers.
2. Paste the following code:
Code for the command with the `!example` trigger:
```
$nomention
Click the button below!
$addButton[no;test;Click;primary]
$addButton[no;button;Button disabled;secondary;yes]
$addButton[yes;https://botdesignerdiscord.com/;Link;link]
```
Code for the command with the `$onInteraction[test]` trigger:
```
$nomention
$editButton[test;Clicked;danger;yes]
$sendMessage[$username hello!]
```

> Note that the interaction ID provided in `$onInteraction[]` is the same as the one provided in `$addButton[]`
> 
> In `$addButton[]`, `yes` is being used for the `new row?` argument so that the button would appear in the next row.
3. Execute command `!example`

![example](https://user-images.githubusercontent.com/113303649/211164994-695cf7b6-b2fa-49e5-a78f-dc21db213a9a.png)

### Example with `$onInteraction` callback:
1. Create two commands with `!example` and `$onInteraction` triggers.
2. Paste the following code:
Code for the command with the `!example` trigger:
```
$nomention
Click the button below!
$addButton[no;test;Click;primary]
$addButton[no;button;Button disabled;secondary;yes]
$addButton[yes;https://botdesignerdiscord.com/;Link;link]
```
Code for the command with the `$onInteraction` trigger:
```
$nomention
$if[$customID==test]
    $editButton[test;Clicked;danger;yes]
    $sendMessage[$username hello!]
$endif
```
> Note that the interaction ID returned by `$customID` will be the same as the one provided in `$addButton[]`
> 
> In `$addButton[]`, `yes` is being used for the `new row?` argument so that the button would appear in the next row.
> 
3. Execute command `!example`

![example](https://user-images.githubusercontent.com/113303649/211164994-695cf7b6-b2fa-49e5-a78f-dc21db213a9a.png)


> How [`$onInteraction`](../../../../callbacks/onInteraction.md) or [`$onInteraction[]`](../../../..//callbacks/onInteractionComplex.md) works?

