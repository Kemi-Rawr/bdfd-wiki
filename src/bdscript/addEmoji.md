# $addEmoji
Adiciona um emoji no servidor.

## Sintaxe
```
$addEmoji[Nome;URL de Imagem;Retornar emoji?]
```

### Parâmetros 
- `Nome` `(Tipo: String || Indicação: Obrigatório)`: O nome do novo emoji.
  
- `URL de Imagem` `(Tipo: URL || Indicação: Obrigatório)`: A imagem do novo emoji. O link tem que ser uma imagem URL válida.
- `Retornar emoji?` `(Tipo: Bool || Indicação: Obrigatório)`: Se deve mostrar o emoji na resposta do bot ou não.

## Examplo
```
$nomention
$argsCheck[>2;Uso desse comando: `k!add-emoji (Nome) (URL)`]
Novo emoji adicionado: $addEmoji[$message[1];$message[2];yes]
```
![IMG_20240802_030853](https://github.com/user-attachments/assets/5eeab899-aa2f-4056-a8b1-8c340990423f)
