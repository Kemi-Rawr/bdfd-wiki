# $authorIcon
Adiciona um ícone na seção do autor na embed.

## Sintaxe 
```
$authorIcon[URL de imagem;(Indexo)]
```

> `$authorIcon[]` não vai funcionar se não tiver um texto fornecido em [`$author[]`](./author.md).

### Parâmetros
- `URL de imagem` `(Tipo: URL || Indicação: Esvaziavel)`: A imagem para o ícone do autor. Isso tem que ser um URL válido.
  
- `Indexo` `(Tipo: Inteiro || Indicação: Opcional)`: Para qual embed o ícone do autor irá ser adicionado. [(aprenda mais)](../resources/embedIndexes.md)

## Examplo
```
$nomention
$authorIcon[$authorAvatar]
$author[⬅️ Esse é o ícone do autor. Esse é o texto do autor.]
```
![Screenshot_20230825-014130~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/09850389-dcc9-4574-bb26-3cb902cdf2ab)
