# $changeCooldownTime
Muda as métricas do cooldown. Essas podem ser usadas nas mensagens de erro do cooldown. Isso pode ser útil para traduções.

## Sintaxe
```
$changeCooldownTime[Dias;Horas;Minutos;Segundos]
```

### Parâmetros
- `Dias` `(Tipo: String || Indicação: Obrigatório)`: O texto para substituir 'Dias'.
- `Hours` `(Tipo: String || Indicação: Obrigatório)`: O texto para substituir 'Horas'.
- `Minutes` `(Tipo: String || Indicação: Obrigatório)`: O texto para substituir 'Minutos'.
- `Seconds` `(Tipo: String || Indicação: Obrigatório)`: O texto para substituir 'Segundos'.

 ### Sub-funções
 
 Nome        | Tipo
------------|---------
`%time-d%`  | Dia
`%time-h%`  | Hora
`%time-m%`  | Minuto
`%time-s%`  | Segundo

## Exemplo
```
$nomention
Olá $displayName!
$changeCooldownTime[dia(s);hora(s);minuto(s);segundo(s)]
$cooldown[10m;Por favor espere %time-m% minutos e %time-s% segundos!]
```
![Screenshot_20231213-153328~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/833b260a-8e6e-4d15-a2d8-62ca67cf2118)

