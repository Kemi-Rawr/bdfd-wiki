# $addSelectMenuOption
Adiciona uma nova opção de select menu a um select menu existente
## Sintaxe
```
$addSelectMenuOption[Menu opção ID;Rótulo;Valor;Descrição;(Padrão?;Emoji;Mensagem ID)]
```

### Parâmetros 
- `Menu opção ID` `(Tipo: String || Indicação: Obrigatório)`: O ID usado em [`$newSelectMenu[]`](./newSelectMenu.md).
  
- `Rótulo` `(Tipo: String || Indicação: Obrigatório)`: O nome da opção.
  
- `Valor` `(Tipo: String || Indicação: Obrigatório)`: São os dados que são passados na callback `$onInteraction[]`. **O valor deve ser único no select menu!**
  
- `Descrição` `(Tipo: String || Indicação: Esvaziável)`: Um texto que aparece abaixo de `Label`.
  
- `Padrão?` `(Tipo: Bool || Indicação: Vagável)`: Se a opção deve ser selecionada por padrão ou não. Padroniza como `no`. (`yes`/`no`) **So pode ter uma opção padrão!**
  
- `Emoji` `(Tipo: Emoji || Indicação: Vagável)`: O emoji que aparece perto do `Label`.
  
- `Mensagem ID` `(Tipo: String || Indicação: Vagável)`: O ID de uma mensagem que deve ser adicionado uma nova opção select menu para um select menu existente. Por padrão é a resposta do bot.

## Examplo
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
