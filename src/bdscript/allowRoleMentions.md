# $allowRoleMentions
Ativa a menções de cargos apenas pelos IDs de cargos fornecidos, enquanto os cargos não fornecidos receberão uma "menção fake" *(O cargo vai ser mencionado, porém usuários não serão notificados)*.

## Sintaxe 
```
$allowRoleMentions[IDs de cargos;...]
```

### Parâmetros 
- `IDs de cargos` `(Tipo: Snowflake || Indicação: Esvaziável)`: Os cargo(s) que podem ser mencionados, deixe vazio para desabilitar menções para todos os cargos. Separe os IDs de cargos usando `;`.

## Example
```
$nomention
$allowRoleMentions[]
Estou mencionando o cargo <@&1102036888145113210>, porém ninguém foi notificado!
```
![Screenshot_20230823-013213~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/e7acd75f-934f-46fd-adb3-77b0a4f1db3f)

