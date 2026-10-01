# Ora 8 · Laboratorio — La prima versione di `calendario-lezioni`

> Al computer · da soli · 18 minuti · si lavora nella cartella di prova della 3ª B

## Cosa facciamo e perché

Ogni anno, a settembre, trasformate la programmazione in un piano: quali argomenti in quali
settimane, dove mettere le verifiche, quanto tempo resta per il recupero. È un lavoro fatto di
conti e di scelte.

Oggi lo fate fare all'agente, ma in un ordine preciso. **Prima** gli fate contare le ore e
dire che cosa non sa, e le risposte le date voi. **Poi** gli fate scrivere una skill che
lavori sempre così. **Infine** la usate, in una sessione nuova, e controllate il risultato.

Quello che ottenete è la prima versione di una skill che potete riusare ogni settembre, su
ogni classe.

## Prima di cominciare

Aprite con l'agente una copia della **cartella di prova**. Vi servono due file, tutti e due in
`02-programmazione/`:

- `programmazione-annuale.md`: le unità della 3ª B e le loro ore;
- `calendario-scolastico-2025-26.md`: inizio e fine delle lezioni, feste, vacanze, uscite.

La 3ª B ha matematica il **lunedì, il mercoledì e il venerdì**.

Facciamo finta che sia **inizio settembre 2025**. Nella stessa cartella c'è anche il diario
delle lezioni già svolte fino a gennaio: l'agente non lo deve usare, e le richieste qui sotto
glielo dicono.

## Passi

### 1 · Le ore e le ipotesi, prima del calendario · 5 minuti

Incollate:

```
Siamo a inizio settembre 2025 e devo pianificare l'anno della 3ª B.
Leggi la programmazione annuale e il calendario scolastico in
02-programmazione (ignora il diario delle lezioni svolte). Non scrivere
ancora il calendario. Prima dimmi:
- quante ore di lezione ho davvero, per quadrimestre, e come le hai
  contate;
- se ci stanno le unità previste, con le verifiche;
- quali informazioni ti mancano e che ipotesi faresti per ciascuna.
Poi fermati e aspetta le mie risposte.
```

Leggete **come** ha contato: se ha usato un piccolo programma, chiedetegli l'elenco dei giorni
in cui non c'è lezione e scorretelo. Se ha contato a mente, chiedetegli di rifarlo con un
programma.

Poi rispondete alle ipotesi, una per una. Non esiste una risposta giusta: sono le vostre
decisioni di docente. Se le ore non bastano, chiedetegli due o tre modi diversi per farcele
stare, e sceglietene uno.

### 2 · Farla scrivere, e leggerla · 6 minuti

Incollate:

```
Adesso trasforma quello che abbiamo fatto in una skill. Chiamala
calendario-lezioni, mettila fra le skill di questo progetto e dimmi in
quale cartella l'hai messa. Rispetta queste regole:
- in ingresso: la programmazione, il calendario scolastico e i giorni
  della settimana in cui la classe ha lezione;
- le ore disponibili si contano giorno per giorno con un piccolo
  programma, non a mente; prima di pianificare mostra il totale per
  quadrimestre e l'elenco dei giorni persi;
- prima di pianificare elenca le ipotesi che devi fare, poi fermati e
  aspetta le mie risposte;
- se le ore non bastano, non comprimere in silenzio: proponi due o tre
  alternative, con quello che costa ciascuna, e lascia scegliere me;
- l'ordine delle unità è quello della programmazione; ogni unità si
  chiude con la sua verifica, e l'ultima verifica di un quadrimestre
  cade almeno una settimana prima della fine;
- lascia ore di margine, scritte nel calendario come margine;
- l'uscita è il file calendario-lezioni.csv, separato da punto e
  virgola, con una riga per lezione: data;giorno;unita;argomento;tipo.
  Il tipo è uno fra lezione, esercitazione, verifica, margine,
  pausa didattica;
- dopo il file, mostrami una tabella con le ore previste e pianificate
  per ogni unità, e l'elenco numerato delle ipotesi e delle decisioni;
- se calendario-lezioni.csv esiste già, non riscriverlo da capo: parti
  da quello, perché potrei averlo corretto a mano.
Tienila sotto le 600 parole.
```

Poi aprite la cartella che vi ha indicato e **leggete `SKILL.md`**. Due domande: *c'è il
punto in cui si ferma a chiedere?* e *c'è scritto che le ore si contano con un programma?* Se
manca qualcosa, fatelo correggere adesso.

### 3 · Usarla davvero · 7 minuti

Aprite una **sessione nuova**, così l'agente non ricorda la conversazione di prima, e
scrivete:

```
Usa la skill calendario-lezioni per la 3ª B, anno 2025/26. Siamo a
inizio settembre: ignora il diario delle lezioni svolte.
```

Se la skill è scritta bene, **non parte subito**: vi mostra le ore e vi chiede le ipotesi.
Rispondete come al passo 1.

Quando ha finito, **non cominciate dalla prima riga del calendario**. Guardate, nell'ordine:

1. la tabella con le ore previste e pianificate: le righe che non tornano sono i tagli;
2. l'elenco delle ipotesi: sono quelle che avete deciso voi?
3. il file: aprite `calendario-lezioni.csv` con un foglio di calcolo. Il numero di righe è
   uguale al totale delle ore che vi ha dato all'inizio?
4. le verifiche: dove cadono? L'ultima del primo quadrimestre lascia il tempo di
   correggerla?

## Da controllare alla fine

- **Le ore sono contate con un programma?** E l'elenco dei giorni persi è giusto per la 3ª B?
  Una festa che cade di sabato, o di martedì, non toglie niente.
- **La skill si è fermata sulle ipotesi?** Se è partita dritta, la regola non ha tenuto: va
  scritta in modo più netto, all'inizio dei passi.
- **C'è margine?** Quante ore, e dove?
- **Se qualcosa è stato tagliato, l'avete deciso voi?**

## Se non arrivate in fondo

Fermatevi al passo 2: una skill scritta dopo aver fatto il lavoro una volta, e letta con
attenzione, è il risultato che conta. Un calendario completo della 3ª B, con le ipotesi
dichiarate, vi verrà dato alla fine: servirà nell'ora 9.

## Chi finisce prima

Chiedete una vista da guardare:

```
Fammi una pagina HTML di sola lettura del calendario: una colonna per
settimana, un colore per tipo di ora, le verifiche in evidenza.
```

Poi aprite il file CSV, spostate a mano una verifica di qualche giorno, e chiedete:

```
Ho spostato una verifica in calendario-lezioni.csv. Riallinea le
lezioni intorno senza rifare il resto, e dimmi che cosa hai cambiato.
```

Se riscrive tutto il file da capo, la regola sull'ultimo punto della skill non ha tenuto.

## A casa, facoltativo · Sulla vostra classe

La programmazione non contiene dati degli studenti: potete usare la skill con la vostra.
Vi servono la programmazione, il calendario della vostra scuola e i giorni in cui avete
lezione in quella classe. Confrontate il totale delle ore con quello che avevate in mente a
settembre.

## Quando avete finito

- Avete una skill, `calendario-lezioni`, che conta le ore con un programma e si ferma sulle
  ipotesi.
- Avete un calendario della 3ª B con una riga per lezione, il margine e l'elenco delle
  decisioni prese.
- Le decisioni su che cosa tagliare, e dove mettere le verifiche, sono state vostre.
