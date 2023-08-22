# $addSelectMenuOption
Adiciona uma nova opção de select menu a um select menu existente
## Sintaxe
```
$addSelectMenuOption[Menu opção ID;Rótulo;Valor;Descrição;(Padrão?;Emoji;Mensagem ID)]
```

### Parameters
- `Menu opção ID` `(Tipo: String || Indicação: Obrigatório)`: O ID usado em [`$newSelectMenu[]`](./newSelectMenu.md).
  
- `Rótulo` `(Tipo: String || Indicação: Obrigatório)`: O nome da opção.
  
- `Valor` `(Tipo: String || Indicação: Obrigatório)`: São os dados que são passados na callback `$onInteraction[]`. **O valor deve ser único no select menu!**
  
- `Descrição` `(Tipo: String || Indicação: Emptiable)`: A text which shows up under the `Label`.
  
- `Default?` `(Type: Bool || Flag: Vacantable)`: Whether the option should be selected by default or not. Defaults to `no`. (`yes`/`no`) **There can be only one default option!**
  
- `Emoji` `(Type: Emoji || Flag: Vacantable)`: The emoji that shows up next to the `Label`.
  
- `Message ID` `(Type: String || Flag: Vacantable)`: The ID of a message that should have a new select menu option added to an existing select menu. By default it's the bot's response.

## Example
```
$nomention
$newSelectMenu[Example;1;1;Choose some option]
$addSelectMenuOption[Example;First;first-option;The first option]
$addSelectMenuOption[Example;Second;second-option;The second option]
$addSelectMenuOption[Example;Third;third-option;The third option]
```
![example](https://user-images.githubusercontent.com/113303649/209933666-9ec8ecfc-e666-4caa-b7cb-b0b3c4cdea02.png)\
![example](https://user-images.githubusercontent.com/113303649/209933373-978c8ade-157f-4991-bb93-929430b4a4eb.png)

> For more info, see the [Select Menu Guide](../guides/general/interactions/selectMenus/aboutSelectMenu.md).
