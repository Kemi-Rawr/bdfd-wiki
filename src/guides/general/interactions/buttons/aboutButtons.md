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


> Se o estilo `link` é usado, o botão **não enviará** alguma interação!

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

## Example
```
$nomention
Hi
$addButton[no;test;Say hello!;primary;no;]
```
![example](https://user-images.githubusercontent.com/16838075/120199057-18c2de00-c223-11eb-9198-997227082a76.png)


# $editButton
Edits an already existing button.

## Syntax
```
$editButton[interaction ID/url;label;style;(disable?;emoji;message ID)]
```

### Parameters
- `interaction ID/url` `(Type: String, URL || Flag: Required)`: Depending on the button type, you either set it to an `interaction ID` which is then used in the `$onInteraction[ID]` callback or a `URL` if it's a link button.
- `label` `(Type: String || Flag: Emptiable)`: The text visible on the button.
- `style` `(Type: Enum || Flag: Required)`: It's used to specify the button's background color. If the button has a link/url you **have to** set this value to `link`. Check [this section](#button-style) for more details.
- `disable?` `(Type: Bool || Flag: Vacantable)`: If set to `yes` the button can't be pressed. Defaults as `no`. _(Optional)_
- `emoji` `(Type: Emoji || Flag: Vacantable)`: Edits an emoji inside the button. Emojis have to be either pasted as *unicode* or be in the following format `<:emoji name:emoji ID>`. _(Optional)_
- `message ID` `(Type: Snowflake || Flag: Vacantable)`: Edits a button in a message with the provided ID. It's important to note that provided message ID author **has to** be the bot. _(Optional)_
## Example
#### Trigger: `$onInteraction[test]`
```
$nomention
$username said hello!
$editButton[test;Say hello!;danger;yes;]
```
![example](https://user-images.githubusercontent.com/113303649/210611967-f15b8c9b-7bd9-4218-a89b-08e93ce7eeb3.png)


# $removeButtons
Removes all buttons from the triggered message.
## Syntax
```
$removeButtons
```
## Example
#### Trigger: `$onInteraction[test]`
```
$nomention
$username removed all buttons from this message
$removeButtons
```
![example](https://user-images.githubusercontent.com/113303649/210621352-ae7334a6-a2de-4fbe-8749-7134f9a73af3.png)

# $removeButtons[]
Removes all buttons from the specified message.
## Syntax
```
$removeButtons[message ID]
```
### Parameters
- `message ID` `(Type: Snowflake || Flag: Required)`: Removes buttons from the message with the provided ID. It's important to note that provided message ID author **has to** be the bot.
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

