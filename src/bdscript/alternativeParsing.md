# $alternativeParsing
Muda a forma que os gatilhos são lidos.

## Sintaxe 
```
$alternativeParsing
```
> Essa função foi adicionada no final de 2019 como um experimento, e pode ser não-instável e quebrar seus comandos. Você não deveria usar `$alternativeParsing` em uma criação de bot público.

## Examplo
1. Crie dois comandos e sete o gatilho `olá` para um comando e `olámundo` para o outro.
2. Adicione a função `$alternativeParsing` no código do comando com o gatilho `olá`.

    Código com o gatilho `olá`:
    ```
    $nomention
    $alternativeParsing
    $description["olá"]
    ```
    Código com o gatilho `olámundo`:
    ```
    $nomention
    $description["olámundo"]
    ```
3. Execute os comandos.
    ### Com `$alternativeParsing`
    ![Screenshot_20230825-002507~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/f0aff97c-4a64-447f-b57d-2055f4c1693b)

    ### Sem `$alternativeParsing`
    ![Screenshot_20230825-002621~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/b05500fe-b470-4a8a-8fe3-6a487737764b)

