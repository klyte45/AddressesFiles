# Sintassi dei prefissi stradali

## Sensi stradali

* `w` Senso unico
* `W` Doppio senso

*Se omesso, applicherà qualsiasi tipo*

## Simmetria della strada
*applicabile solo a strade a senso unico*

* `s` Simmetrico
* `S` Asimmetrico

*Se omesso, applicherà qualsiasi tipo*

## Indicatore autostradale

* `h` Solo autostrada
* `H` Solo tipi di strada urbana

*Se omesso, applicherà qualsiasi tipo*

## Uscite stradali

* `f` Uscita che parte da un'autostrada diretta a un altro percorso più piccolo o urbano
* `i` Uscita che termina su un'autostrada e proveniente da un'autostrada minore
* `e` Uscita che collega strade di uguale dimensione

*Se omesso, applicherà qualsiasi tipo*

**NOTA:** Si applica solo alle autostrade a senso unico (richiede anche `hw`, anche se omesso o posizionato al contrario).

### Ordine di confronto delle dimensioni del percorso
* Percorso continuo (quello che ha la continuazione ha la priorità)
* È un'autostrada (le strade urbane non hanno priorità)
* Numero di tracce (più grande è, maggiore sarà la priorità)
* Larghezza della carreggiata (più grande è, maggiore sarà la priorità)

## Tipo di sentiero
* `G` Sentieri a livello del suolo
* `B` Sentieri sopraelevati e ponti
* `T` Tunnel
* `D` Dighe

*Se omesso, applicherà qualsiasi tipo*

## Numero corsie

* `(X,Y)` da X (incluso) a Y (escluso Y). Quando X o Y viene omesso, X = 0 e Y = 255.
* `(Z)` esattamente Z corsie.

*Se omesso, applicherà un numero qualsiasi di corsie (equivalente a `(,)`)*

## Larghezza percorso

* `[X,Y]` da X (incluso) a Y (escluso Y) metri di larghezza. Quando X o Y vengono omessi, X = 0 e Y = 999.
* `[Z]` esattamente Z metri di larghezza.

*Se omesso, applicherà qualsiasi dimensione (equivalente a `[,]`)*

## Tipo di autostrada (dal 3.0)
* `p` è assegnato a un registro del tipo di autostrada
* `P` non è assegnato a un registro del tipo di autostrada

## Nome fisso del seed (dal 3.0)
* `n` Ha un nome fisso
* `N` Non ha un nome fisso

## Argomenti disponibili per la nomenclatura
Utilizzare queste stringhe per fare riferimento alle seguenti variabili nel formato:

ID | Descrizione | Dalla versione | Osservazione
-- | ----------- | -------------- | ------------
`{0}` | Nome generato da file di nomi (impostazione predefinita per strade e autostrade)| 1.0 | -
`{1}`| Nome della strada di destinazione | 1.0 | **richiede che la voce si applichi solo a strade a senso unico!**
`{2}` | Fonte del nome della strada | 1.0 | **richiede che la voce si applichi solo a strade a senso unico!**
`{3}` | Traccia chilometrica di origine, in chilometri e come valore intero | 1.0 | **richiede che la voce si applichi solo a strade a senso unico!**
`{4}` | Traccia chilometrica di provenienza, in chilometri e con un decimale | 1.0 | **richiede che la voce si applichi solo a strade a senso unico!**
`{5}` | Distretto/città vicina di origine | 1.1 | -
`{6}` | Distretto/città vicina di destinazione | 1.1 | -
`{7}` | Direzione cardinale della strada (8 direzioni) |1.1| **richiede che la voce si applichi solo a strade a senso unico!**
`{8}` | Codice lungo di tipo autostradale | 3.0 |**richiede `p`**
`{9}` | Nome forzato del tipo di autostrada | 3.0 |**richiede `n`**
`{10}`| Codice breve del tipo di autostrada | 3.0 |**richiede `p`**