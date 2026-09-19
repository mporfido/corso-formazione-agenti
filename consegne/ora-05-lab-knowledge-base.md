# Ora 5 · Laboratorio — La vostra knowledge base

> Al computer · da soli · 20 minuti · si crea una cartella nuova · servono tre-cinque fonti
> della vostra disciplina

## Cosa facciamo e perché

Nell'ora 4 avete scritto chi siete. Adesso date all'agente il materiale su cui lavorare: le
fonti della vostra disciplina, organizzate in modo che le ritrovi da solo e che vi dica
sempre da dove ha preso quello che afferma.

La parte interessante è come le organizzerete. Non dovete deciderlo voi. Andrej Karpathy ha
scritto due pagine in cui descrive come si costruisce una knowledge base mantenuta da un
agente: come si dividono le cartelle, che cosa va nel file-guida, che cosa succede quando si
aggiunge una fonte. Voi consegnate quel testo all'agente, gli dite di quale argomento vi
occupate, e lui prepara tutto.

È il senso di questa mezz'ora. Una descrizione scritta bene da qualcun altro basta a montare
un impianto intero, senza che voi dobbiate inventarlo o conoscerlo in anticipo.

## Prima di cominciare

Preparate **tre-cinque fonti** della vostra disciplina: le slide di un corso, un PDF di
normativa, un capitolo, un articolo, i vostri appunti. Bastano file che avete già.

Se siete arrivati senza materiale, su Classroom trovate l'archivio
`ora-05-fonti-esempio.zip`. Contiene tre documenti pubblici di didattica trasversale — le
Linee guida del Ministero sull'intelligenza artificiale e le due raccomandazioni europee su
competenze chiave e qualifiche — e dentro c'è un `LEGGIMI.md` che spiega come usarli.

## Passi

### 1 · La cartella · 3 minuti

Create una cartella nuova e vuota, per esempio `knowledge-base`, in un posto che
ritroverete. Apritela con l'agente.

Metteteci dentro le vostre fonti. Per ora lasciatele alla rinfusa: come sistemarle lo decide
l'agente fra un minuto.

### 2 · La consegna all'agente · 7 minuti

Incollate questa richiesta, con il vostro argomento al posto della parentesi quadra:

```
Leggi questo testo:
https://gist.githubusercontent.com/karpathy/442a6bf555914893e9891c11519de94f/raw/ac46de1ad27f92b28ac95459c782c07f6b8c964a/llm-wiki.md

Descrive un modo di costruire una knowledge base mantenuta da un agente.
Seguendo quelle linee guida, prepara in questa cartella la mia wiki su
[argomento]. Crea le cartelle, scrivi il file-guida con le convenzioni e le
operazioni, e crea l'indice e il registro. Poi spiegami in poche righe le
scelte che hai fatto.
```

Al posto di `[argomento]` scrivete la vostra materia e il taglio che vi interessa. Per
esempio «la didattica della matematica al biennio», oppure «la valutazione per competenze in
un istituto tecnico».

Se l'agente vi chiede il permesso di aprire un indirizzo internet, dategliela: senza quel
testo non può fare il resto.

Quando ha finito, **leggete il file-guida che ha scritto**, prima di andare avanti. È il
documento che regolerà tutto il lavoro successivo. Se una convenzione non vi convince,
ditelo a voce e fatela cambiare: «i nomi dei file li voglio in italiano», «aggiungi un campo
con l'anno della fonte», «le pagine di sintesi le voglio più corte».

### 3 · Le vostre fonti · 10 minuti

Adesso fate entrare il materiale:

```
Ingerisci le fonti che ho messo nella cartella, una alla volta. Per ognuna
fermati e dimmi che cosa hai scritto, prima di passare alla successiva.
```

Leggete almeno una sintesi mentre l'agente lavora. Se dice cose che voi non direste,
correggetela subito: è più facile adesso che fra dieci pagine.

Quando ha finito, fate una domanda vera, di quelle che fareste a un collega:

```
[la vostra domanda]. Dimmi da quali pagine e da quali fonti hai preso ogni cosa.
```

Poi fate la **domanda di controllo**. Scegliete un argomento che sapete con certezza non
essere nelle vostre fonti, e chiedete:

```
Nelle mie fonti, che cosa si dice di [argomento assente]? Se non c'è, dimmelo.
```

Chi sta usando il pacchetto d'esempio trova già una domanda pronta nel suo `LEGGIMI.md`.

Se l'agente risponde lo stesso, con affermazioni ragionevoli e nessuna citazione, sta usando
le sue conoscenze generali e ve le sta presentando come se venissero dal vostro materiale.
Aggiungete al file-guida una riga come questa, e rifate la domanda:

```markdown
- In ogni risposta cita i file da cui prendi le informazioni. Se una cosa non
  la trovi nelle pagine o nelle fonti, dillo invece di rispondere lo stesso.
```

## Da controllare alla fine

- **Le fonti sono intatte?** L'agente non deve aver modificato, rinominato o spostato niente
  dentro la cartella delle fonti.
- **Il file-guida spiega le operazioni?** Deve dire che cosa fare quando si aggiunge una
  fonte, quando si pone una domanda e quando si controlla la salute della wiki.
- **Ogni pagina cita la sua fonte?** Aprite una pagina a caso e cercate il riferimento.
- **L'indice le elenca tutte?** Una pagina che non compare nell'indice, per l'agente è come
  se non esistesse.
- **Alla domanda di controllo ha ammesso di non sapere?** È la prova che conta.

## Se non arrivate in fondo

Fermatevi al passo 2 e portatevi a casa la cartella. Il file-guida che l'agente ha scritto è
già la parte difficile: le fonti potete ingerirle con calma, una alla volta, nei prossimi
giorni.

## A casa, facoltativo · La seconda fonte

Aggiungete una fonte sola alla vostra wiki e guardate che cosa succede.

1. Mettete il file nella cartella delle fonti e chiedete all'agente di ingerirlo.
2. Contate quante pagine tocca. Di solito ne aggiorna diverse, non soltanto quella nuova.
3. Chiedete: «Questa fonte contraddice qualcosa che c'era già?».

È la differenza fra una wiki e una cartella di PDF. Ogni materiale che aggiungete migliora
anche quello che c'era prima.

## Quando avete finito

- Avete una cartella con le vostre fonti intatte, le pagine di sintesi scritte dall'agente e
  un indice che le elenca.
- Il file-guida lo ha scritto l'agente, e voi lo avete letto e corretto.
- Alla domanda di controllo l'agente vi ha detto che l'informazione non c'era.
