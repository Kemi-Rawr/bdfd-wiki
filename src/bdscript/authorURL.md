# $authorURL
Adiciona um hyperlink no texto do autor.

## Sintaxe 
```
$authorURL[URL;(Indexo)]
```
> `$authorURL[]` não vai funcionar se não tiver nenhum texto fornecido em [`$author[]`](./author.md).

### Parâmetros 
- `URL` `(Tipo: URL || Indicação: Esvaziável)`: O link para setar como o hyperlink do autor.
  
- `Indexo` `(Tipo: Inteiro || Indicação: Opcional)`: Para qual embed o autor URL irá ser adicionado. [(aprenda mais)](../resources/embedIndexes.md)

## Examplo
```
$nomention
$author[Clique em mim para visitar a website BDFD!]
$authorURL[https://botdesignerdiscord.com]
```
![Screenshot_20230825-124148~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/2b95c698-e283-47b2-b4bf-085b03be9e56)
![Screenshot_20230825-124208~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/8b9e6376-b0a1-4231-8fd4-75b34b9f4166)

