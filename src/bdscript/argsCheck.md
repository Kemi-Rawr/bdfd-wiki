# $argsCheck
Quando essa função é usada, o comando so pode ser executado se a mensagem do usuário conter uma quantidade específica de argumentos (palavrad).

## Sintaxe
```
$argsCheck[Quantos?;Mensagem de erro]
```

### Parameters
- `Quantos?` `(Tipo: HowMany || Indicação: Obrigatório)`: Quantos argumentos devem estar na mensagem do usuário.
   > Se você quiser que os usuários tenham **3 ou mais argumentos** em suas mensagem, você pode usar `>3`. Se você quiser que os usuários tenham **menos que 3 argumentos** em suas mensagem, você pode usar `<3`. Se você quiser que os usuários tenham **exatos 3 argumentos** em suas mensagem, coloque `3`. 
- `Mensagem de erro` `(Tipo: String || Indicação: Esvaziável)`: A mensagem que o bot irá mandar se o usuário tiver muitos/poucos argumentos.

## Examplo
```
$nomention
$argsCheck[>1;❌ forneça algo para eu falar!]
$message
```
![Screenshot_20230825-011609~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/fe6ce8db-2848-4b5d-8f87-b408cfa94b1e)
