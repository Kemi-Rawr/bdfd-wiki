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
    ``` discord yaml
    - user_id: 729343563401265193
      username: Nicky
      color: "#EE7908"
      content: |
        hello
    
    - user_id: 566613317972394004
      username: Wiki Bot
      color: "#748BD4"
      bot: true
      verified: true
      content: <none>
      embed:
        description: "\"hello\""
    
    - user_id: 729343563401265193
      username: Nicky
      color: "#EE7908"
      content: |
        helloworld
    
    - user_id: 566613317972394004
      username: Wiki Bot
      color: "#748BD4"
      bot: true
      verified: true
      content: <none>
      embed:
        description: "\"helloworld\""
    ```
    \
    ### Sem `$alternativeParsing`
    ``` discord yaml
    - user_id: 729343563401265193
      username: Nicky
      color: "#EE7908"
      content: |
        hello
    
    - user_id: 566613317972394004
      username: Wiki Bot
      color: "#748BD4"
      bot: true
      verified: true
      content: <none>
      embed:
        description: "\"hello\""
    
    - user_id: 729343563401265193
      username: Nicky
      color: "#EE7908"
      content: |
        helloworld
    
    - user_id: 566613317972394004
      username: Wiki Bot
      color: "#748BD4"
      bot: true
      verified: true
      content: <none>
      embeds:
      - description: "\"helloworld\""
      - description: "\"hello\""
    ```
