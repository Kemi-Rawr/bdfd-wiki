# $addEmoji
Adiciona um emoji no servidor.

## Sintaxe
```
$addEmoji[Nome;Imagem URL;Retornar emoji?]
```

### Parâmetros 
- `Nome` `(Tipo: String || Indicação: Obrigatório)`: O nome do novo emoji.
  
- `Imagem URL` `(Tipo: URL || Indicação: Obrigatório)`: A imagem do novo emoji. O link tem que ser uma imagem URL válida.
- `Retornar emoji?` `(Tipo: Bool || Indicação: Obrigatório)`: Se deve mostrar o emoji na mensagem do bot ou não.

## Examplo
```
$nomention
$argsCheck[>2;Uso desse comando: `!add-emoji (URL) (Nome)`]
Novo emoji adicionado: $addEmoji[$replaceText[$message;$message[1];;1];$message[1];yes]
```
![Screenshot_20230821-220903~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/490435a0-da3d-44f2-bac1-491729c26f76)
