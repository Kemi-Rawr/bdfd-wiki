# $botListHide
Esconde este comando de aparecer na lista de comandos DBL (Se o bot estiver em [**Bot Designer List**](https://botdesignerlist.com)).

## Sintaxe
```
$botListHide
```
> Esta função não esconde o comando de [`$botCommands[]`](./botCommands.md).

## Exemplo
1. Crie dois comandos e sete o gatilho `!ping` para um comando e `!secret` para o outro.
2. Adicione a função `$botListHide` no código do comando com o gatilho `!secret`.

   Código com o gatilho `!secret`:
   ```
   $nomention
   Este é um comando secreto! 🤫
   $botListHide
   ```

   Código com o gatilho `!ping`:
   ```
   $nomention
   Pong!
   $botListDescription[Ping? Pong!]
   ```
3. Execute os comandos

   ![Screenshot_20231212-035858~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/cf8e9d9c-5ebb-4547-98d4-0acf28aa2610)


   - Com `$botListHide`\
     ![example](https://user-images.githubusercontent.com/113303649/210349185-677b00f3-df10-4443-a9b5-25ec9c2c2e29.png)

   - Sem `$botListHide`\
     ![example](https://user-images.githubusercontent.com/113303649/210350126-b99c73bd-e684-4f5e-a01c-f32c40c54c20.png)
