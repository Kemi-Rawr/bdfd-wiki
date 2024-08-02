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
- `Alinhar?` `(Tipo: Bool || Indicação: Opcional)`: Se definido como `yes`, fields irão aparecer na mesma linha. Porém, se você tiver mais que 3 fields (ou os fields são muito longos) com alinhar ativado, o bot vai retornar filas com 3 fields (2 se tiver uma thumbnail) em cada fila. É definido como `não` por padrão.
  
- `Indexo` `(Tipo: Inteiro || Indicação: Opcional)`: Adiciona o field a uma embed com o número indexo especificado. [(Aprenda mais)](../resources/embedIndexes.md)

> 💡 Fields alinhados podem não aparecer alinhados em alguns dispositivos mobile.

## Examplo

### Sem field alinhado
```
$nomention
$addField[O nome do field 1!;O valor do field 1!]
$addField[O nome do field 2!;O valor do field 2!]
$addField[O nome do field 3!;O valor do field 3!]
```
![Screenshot_20230823-134333~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/fa7c8cf6-f0ed-4a29-89e9-ff0c45beb261)


### Com field alinhado
```
$addField[O nome do field 1!;O valor do field 1!;yes]
$addField[O nome do field 2!;O valor do field 2!;yes]
$addField[O nome do field 3!;O valor do field 3!;yes]
```
![Screenshot_20230822_105729-1](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/a2edf8d3-4b0e-4a53-b4f2-a7bb72b942b1)

