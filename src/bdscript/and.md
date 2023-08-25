# $and
Retorna `true` se todas as condições fornecidas são verdadeiras, ou se não `false` é retornado.

## Sintaxe
```
$and[Condições;...]
```

### Parameters
- `Condições` `(Tipo: String || Indicação: Obrigatório)`: Verificações que serão realizadas. Todas as condições devem ser verdadeiras para essa função retornar `true`. Separe as condições usando `;`.

### Operadores
`==` - Igual

`!=` - Não Igual

`<` -  Menor Que

`>` - Maior Que

`>=` - Maior Que ou Igual a

`<=` - Menor Que ou Igual a
- Esses operadores podem variar no significado baseado na ordem ou na intenção da declaração do If.
- Se você estiver usando texto como `x` e/ou `y`, Você não pode usar qualquer outro operador além de == e `!=`. Porém para números, você pode usar qualquer operador na lista acima.

## Examplo
```
$nomention
$and[$nickname==Kemi v2;$message==Olá]
```
![Screenshot_20230825-005645~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/05826074-e185-4ced-a354-5106234b847d)
![Screenshot_20230825-005724~2](https://github.com/Kemi-Rawr/bdfd-wiki/assets/111205130/c655e687-0ab0-4a27-a29e-9758476e9d5f)


> Para mais informações, Veja a [Guia de If](../guides/ifStatements.md).
