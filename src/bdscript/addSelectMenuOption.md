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
  
- `Mensagem ID` `(Tipo: String || Indicação: Vagável)`: O ID de uma mensagem que deve ser adicionado uma nova opção de select menu para um select menu existente. Por padrão é a resposta do bot.

## Examplo
```
$nomention
$newSelectMenu[Examplo;1;1;Escolha alguma opção]
$addSelectMenuOption[Examplo;Primeira;primeira-opção;A primeira opção]
$addSelectMenuOption[Examplo;Segunda;segunda-opção;A segunda opção]
$addSelectMenuOption[Examplo;Terceira;terceira-opção;A terceira opção]
```
![Screenshot_20230822-123721~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/3248bb47-fb7c-4cba-a06e-f45954cd3c2f)
![Screenshot_20230822-123743~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/f8218a54-9736-4213-bb4b-ccfb2d966e70)

> Para mais informações, veja a [Guia de Select Menu](../guides/general/interactions/selectMenus/aboutSelectMenu.md).
