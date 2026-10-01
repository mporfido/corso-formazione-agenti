# Ora 8 · Demo — Il calendario, chiesto e basta

> Conduce il formatore · circa 5 minuti · slide 6 di `slides/ora-08.html`

## Prima della lezione

- [ ] Una copia pulita di `cartella-di-prova/`, aperta nell'agente, con `AGENTS.md` al suo
      posto e il file `02-programmazione/calendario-scolastico-2025-26.md`.
- [ ] Nessuna skill `calendario-lezioni` installata nella cartella: la demo mostra l'agente
      senza istruzioni.
- [ ] Un foglio di calcolo aperto a parte, per contare le righe del calendario che uscirà.

## Passi

1. Sessione nuova. Incolla la richiesta e lascia lavorare. Ci vogliono un paio di minuti:
   intanto torna alla slide e leggi i quattro punti da guardare.
2. Quando ha finito, **non leggere il calendario dall'inizio**. Cerca, nell'ordine:
   - il numero di ore o di lezioni che ha contato, e se dice come;
   - dove sono le verifiche, e se le ha messe dentro o fuori dalle ore delle unità;
   - che cosa ha fatto con la pausa didattica del 9-13 febbraio e con le assemblee;
   - se ha tolto ore a qualche unità, e se lo dice.
3. Confronta le ore con la slide 7: **98 lezioni**, 51 nel primo quadrimestre e 47 nel
   secondo.
4. Chiudi con la domanda: *quante di queste decisioni avreste preso nello stesso modo?*

## La richiesta

```
Siamo a inizio settembre 2025 e devo pianificare l'anno della 3ª B:
ignora il diario delle lezioni svolte. A partire dalla programmazione
annuale e dal calendario scolastico, fammi il calendario delle lezioni
di tutto l'anno, lezione per lezione.
```

## I numeri di controllo

| | 1° quad. | 2° quad. | Anno |
|---|---:|---:|---:|
| Lunedì, mercoledì e venerdì dal 15/09 al 05/06 | 60 | 54 | 114 |
| Giorni persi | 9 | 7 | 16 |
| **Lezioni** | **51** | **47** | **98** |
| Ore delle unità in programmazione | 48 | 42 | 90 |

I 16 giorni persi: ven 17/10 (uscita); lun 08/12; lun 22/12, mer 24/12, ven 26/12, lun 29/12,
mer 31/12, ven 02/01, lun 05/01 (Natale); lun 16/02 (Carnevale); ven 03/04, lun 06/04
(Pasqua); mer 22/04, ven 24/04 (viaggio); ven 01/05; lun 01/06 (ponte).

**Non tolgono niente alla 3ª B:** sabato 1/11, martedì 17/02 (Carnevale), sabato 25/04,
martedì 2/06. Se l'agente li sottrae, sta contando per settimane e non per giorni: è l'errore
della slide 8.

Con 6 verifiche e 3 ore di pausa didattica servono 99 ore: **non ci sta**, prima ancora di
correggere una verifica. La programmazione dichiara 99 ore annue ma le unità ne sommano 90:
se l'agente considera le verifiche comprese nelle ore delle unità, «ci sta», ma solo perché
ha deciso lui.

Una soluzione completa, con le ipotesi dichiarate, è in `materiali/ora-08-calendario-pronto/`.

## Che cosa far notare

- **Il risultato sembra ottimo.** Una tabella lunga e ordinata, con i nomi degli argomenti
  giusti. È proprio per questo che va letta partendo dalle scelte, non dalla prima riga.
- **Le scelte silenziose.** Non si sa in anticipo quali farà: verifiche dentro le unità o
  fuori, assemblee ignorate o stimate, pausa di febbraio riempita con argomenti nuovi. Nessuna
  è un errore di calcolo; tutte sono decisioni didattiche prese senza chiedere.
- **Se qualcosa manca, cercatelo in fondo.** Quando le ore non bastano, di solito si accorcia
  l'ultima unità (le funzioni) o si comprimono tutte. È il ponte verso le slide 11 e 12.

## Se qualcosa va storto

- **L'agente si ferma e fa domande prima di pianificare**: ottimo, succede con i modelli più
  prudenti. Rispondi a una domanda sola («le verifiche sono in più») e fagli notare che le
  altre ipotesi non le ha chieste. Il punto della slide 11 diventa: *qui l'ha fatto da solo,
  la skill glielo farà fare sempre*.
- **L'agente usa il diario delle lezioni svolte** e copia le date delle verifiche vere
  (16/10, 27/11, 22/01): la frase «ignora il diario» è stata persa. Ripeti la richiesta in una
  sessione nuova.
- **Il calendario è per settimane, non per lezione**: va bene lo stesso. Chiedi quante ore
  ha la settimana del 27 aprile (sono 2: il 1° maggio è venerdì) e quella del 20 aprile (è 1:
  il viaggio d'istruzione).
- **Ci mette troppo**: interrompi dopo il primo quadrimestre e lavora su quello. I numeri da
  confrontare sono 51 lezioni e 48 ore di unità.
