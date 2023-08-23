# $addField
Adiciona um field em uma embed.

## Sintaxe
```
$addField[Nome;Valor;(Alinhar?;Indexo)]
```

> 📌 Você pode adicionar 25 fields por embed.

### Parâmetros 
- `Nome` `(Tipo: String || Indicação: Obrigatório)`: O nome do field. Não pode ultrapassar mais que 256 caracteres.
  
- `Valor` `(Tipo: String || Indicação: Obrigatório)`: O valor do field. Não pode ultrapassar mais que 1024 caracteres.
- `Alinhar?` `(Tipo: Bool || Indicação: Opcional)`: Se `yes`, fields irão aparecer na mesma linha. Porém, Se você tem mais que 3 fields (ou os fields são muito longos) com alinhar ativado, O bot vai retornar filas com 3 fields (2 se tiver uma thumbnail) em cada fila. É setado como não por padrão.
  
- `Indexo` `(Tipo: Inteiro || Indicação: Opcional)`: Adiciona o field a uma embed com o número indexo especificado. [(Aprenda mais)](../resources/embedIndexes.md)

> 💡 Fields alinhados podem não aparecer alinhados em alguns dispositivos mobile.

## Examplo

### Sem field alinhado
```
$nomention
$addField[The field name 1!;The field value 1!]
$addField[The field name 2!;The field value 2!]
$addField[The field name 3!;The field value 3!]
```
![Screenshot_20230823-133754~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/8ef38c51-a093-45e3-ad46-0420ebc02c49)

### Com field alinhado
```
$addField[O nome do field 1!;O valor do field 1!;yes]
$addField[O nome do field 2!;O valor do field 2!;yes]
$addField[O nome do field 3!;O valor do field 3!;yes]
```
![Screenshot_20230823-133754~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/4d7f6265-aa3e-4aa7-80db-9968df6337f2)
