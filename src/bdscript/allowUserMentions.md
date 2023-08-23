# $allowUserMentions
Ativa menções de usuários apenas pelos IDs de usuários fornecidos, enquanto o usuário não fornecido irá receber uma "menção falsa" *(o usuário irá ser mencionado, mas não irá ser notificado)*.

## Sintaxe 
```
$allowUserMentions[IDs de usuários;...]
```

### Parameters
- `User IDs` `(Type: Snowflake || Flag: Emptiable)`: The user(s) that can be pinged, leave empty to disable pings for every user. Separate user IDs using `;`.

## Example
```
$nomention
$allowUserMentions[]
Hi <@696368083517964288>! I mentioned you, but you didn't get pinged.
```

``` discord yaml
- user_id: 803569638084313098
  username: RainbowKey
  avatar: https://github.com/NilPointer-Software/bdfd-wiki/assets/113303649/a9034fd5-40c2-4320-a408-2f2ee0071d9d
  color: "#E67E22"
  content: |
    !example
- username: BDFD Support
  avatar: https://github.com/NilPointer-Software/bdfd-wiki/assets/113303649/e5fdc906-6c14-4e19-91c0-4ce95b852c61
  color: "#378afa"
  bot: true
  verified: true
  content: |
    Hi <@Spen>! I mentioned you, but you didn't get pinged.
```
