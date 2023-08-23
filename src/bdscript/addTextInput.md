# $addTextInput
Adiciona um novo campo de text input em uma modal.

## Sintaxe
```
$addTextInput[Text input ID;Estilo;Rótulo;(Comprimento mínimo;Comprimento máximo;Obrigatório?;Valor;Espaço reservado)]
```

> 📌 Você pode adicionar até 5 campos de text input em uma modal.

### Parâmetros 
- `Text input ID` `(Tipo: String || Indicaçãp: Obrigatório)`: O ID que é usado para retirar a entrada de texto do campo. **Esse valor deve ser único!**
  
- `Estilo` `(Tipo: Enum || Indicação: Obrigatório)`: O estilo de text input, pode ser `short` ou `paragraph`.
  
- `Rótulo` `(Tipo: String || Indicação: Obrigatório)`: O nome do campo de text input. Esse valor deve ser menor que ou igual a 45 caracteres.
- `Comprimento mínimo` `(Tipo: Inteiro || Indicação: Vagável)`: Mínimo número de caracteres que um usuário deve inserir. Esse valor deve ser um inteiro entre 0 e 4000, e não pode ser maior que o `Comprimento máximo`.
  
- `Comprimento máximo` `(Tipo: Inteiro || Indicação: Vagável)`: Número máximo de caracteres que um usuário deve inserir. Esse valor deve ser um inteiro entre 0 e 4000, e não pode ser menor que o `Comprimento mínimo`.
  
- `Obrigatório?` `(Tipo: Bool || Indicação: Opcional)`: Se um usuário deve preencher o campo de text input ou não. Padroniza como `yes`. (`yes`/`no`)
  
- `Valor` `(Type: String || Flag: Vagavél)`: O texto que é escrito por padrão no campo de text input. Esse valor deve ser menor que ou igual a 4000 caracteres e não ser menor que o `Comprimento mínimo` e não maior que o `Comprimento máximo`.
  
- `Texto reservado` `(Tipo: String || Indicação: Vagável)`: O texto que é mostrado se o campo de text input é vazio. Esse valor deve ser menor que ou igual a 100 caracteres.

### Estilos
- `short` - Um campo de text input pequeno.
- `paragraph` - Um campo de text input grande.

![Screenshot_20230823-000538~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/113942e4-3956-4108-a9ec-0cfa62ab3e5a)


## Examplo
```
$nomention
$newModal[modal;Biografia de Usuário]
$addTextInput[modalInput1;short;Qual é o seu nome?;3;30;yes;;Mikołaj]
$addTextInput[modalInput2;short;Quais são os seus pronomes?;2;30;yes;;Ele/Dele]
$addTextInput[modalInput3;paragraph;Pode falar um pouco sobre você?;5;1000;no;;I am a Developer]
```
![Screenshot_20230823-001425~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/49a5eaef-4a9a-452e-8da4-45b977208bd2)


> Para mais informações, veja a [Guia de Modals](../guides/general/interactions/modals/aboutModals.md).
