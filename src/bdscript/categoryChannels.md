# $categoryChannels
Lista todos os canais da categoria dada.

## Sintaxe
```
$categoryChannels[ID da Categoria;Separador;(Opção)]
```

### Parâmetros 
- `ID da Categoria` `(Tipo: Snowflake || Indicação: Obrigatório)`: A categoria para qual listar os canais. 
- `Separador` `(Tipo: String || Indicação: Esvaziável)`: O separador para usar enquanto separa as propriedades canais.
- `Opção` `(Tipo: Enum || Indicação: Opcional)`: Qual propriedade pegar dos canais da categoria. O padrão é `name`. Veja [abaixo](#options) para mais informação.

### Opções 
- `name` - Os nomes dos canais.
- `id` - Os IDs dos canais.
- `mention` - As menções dos canais.
- `count` - A quantidade de canais na categoria.

> A opção `count` não lista nada, ao invés ela vai retornar o número de canais abaixo da categoria dada.

## Exemplo
```
$nomention
$categoryChannels[$categoryID[Genérico]; ;mention]
```
![Screenshot_20231213-023013~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/6fe802d8-0166-4c48-b84a-7f8d4a06fa7b)
> [Como `$categoryID[]` functiona?](./categoryID.md)
