# Sintaxe para prefixo de ruas

## Sentidos da via

* `w` Sentido único
* `W` Sentido duplo

*Quando omitido, servirá para qualquer um dos tipos*

## Simetria da via 
*aplicável quando via de sentido duplo apenas*

* `s` Via simétrica
* `S` Via assimétrica

*Quando omitido, servirá para qualquer um dos tipos*

## Indicador de rodovia

* `h` Apenas rodovias
* `H` Apenas vias urbanas

*Quando omitido, servirá para qualquer um dos tipos*

## Saídas de rodovias

* `f` Saída iniciando em uma rodovia com destino a outra via menor ou urbana
* `i` Saída que termina em uma rodovia com origem em rodovia menor
* `e` Saída que liga rodovias de igual tamanho

*Quando omitido, servirá para qualquer um dos tipos*

**OBSERVAÇÃO:** Só se aplica a rodovias de sentido único (implica em `hw` também, mesmo se omitido ou colocado inverso).

### Ordem de comparação de tamanho de vias
* Via contínua (aquela que tem continuação tem prioridade)
* É uma rodovia (vias urbanas não tem prioridade)
* Quantidade de faixas (quanto maior, mais prioridade)
* Largura da via (quanto maior, mais prioridade)

## Tipo de via
* `G` Vias ao nível do solo
* `B` Vias elevadas e pontes
* `T` Túneis
* `D` Barragem

*Quando omitido, servirá para qualquer um dos tipos*

## Quantidade de faixas

* `(X,Y)` de X (inclusive) a Y (excluindo Y) faixas. Quando X ou Y é omitido, X=0 e Y=255.
* `(Z)` exatamente Z faixas.

*Quando omitido, servirá para qualquer quantidade de faixas (equivalente a `(,)`)*

## Largura da via

* `[X,Y]` de X (inclusive) a Y (excluindo Y) metros de largura. Quando X ou Y é omitido, X=0 e Y=999.
* `[Z]` exatamente Z metros de largura.

*Quando omitido, servirá para qualquer largura (equivalente a `[,]`)*

## Argumentos disponíveis para nomenclatura
Use estes números entre chaves (`{X}`) para referenciar as seguintes variáveis:

* 0 = Nome gerado dos arquivos de nome (padrão para ruas e rodovias)
* 1 = Nome da estrada de destino **(implica em o registro servir apenas para via de mão única!)**
* 2 = Nome da estrada de origem **(implica em o registro servir apenas para via de mão única!)**
* 3 = Quilometragem da via de origem, em km e valor inteiro **(implica em o registro servir apenas para via de mão única!)**
* 4 = Quilometragem da via de origem, em km e valor com uma casa decimal **(implica em o registro servir apenas para via de mão única!)**
