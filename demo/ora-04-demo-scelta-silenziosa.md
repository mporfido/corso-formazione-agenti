# Ora 4 · Demo — La scelta silenziosa

> Conduce il formatore · circa 6 minuti · slide 6 di `slides/ora-04.html`

## Prima della lezione

- [ ] Una copia pulita di `cartella-di-prova/`, aperta nell'agente.
- [ ] **Il file-guida spento.** Rinomina `AGENTS.md` (vale per questa demo e per la
      successiva):

  ```
  cd cartella-di-prova
  ren AGENTS.md AGENTS.md.off
  ```

  Su Mac o Linux: `mv AGENTS.md AGENTS.md.off`. `CLAUDE.md` e `GEMINI.md` restano al loro
  posto: rimandano a un file che non c'è più, e l'agente va avanti senza istruzioni.
- [ ] **Memoria automatica spenta o vuota**, se il prodotto ce l'ha (vedi slide 13): se ha
      già annotato qualcosa sulla cartella di prova, la prova non è pulita.
- [ ] Per la seconda metà: **due postazioni affiancate** oppure due sessioni nuove una dopo
      l'altra sullo stesso schermo.

## Passi

1. Sessione nuova. Incolla la richiesta e lascia che produca la tabella.
2. Controlla prima che i conti siano giusti (numeri qui sotto). Di solito lo sono: dillo ad
   alta voce, perché il punto è un altro.
3. Porta l'attenzione su **Caruso**: quale media ha scritto? Mostra la tabella della slide
   con le tre letture.
4. Chiedi all'agente come ha deciso (seconda richiesta).
5. Stessa identica richiesta in una **sessione nuova**, sull'altra postazione. Confronta le
   due tabelle.

## Le richieste

```
Guarda la cartella. Fammi una tabella con la media del primo quadrimestre
di ogni studente.
```

```
Come hai deciso di calcolare la media? Quali alternative avevi?
```

## Numeri di controllo

Medie degli scritti, con gli assenti (`ASS`) esclusi: **Marchetti 4,5** · **Esposito 4,5**
· **Sanna 6,25**.

**Caruso Matteo** — scritti 4,5 · 4,0 · 5,0; un solo orale, 6,0.

| Come si calcola | Media |
|---|---|
| Media di tutti e quattro i voti | **4,9** |
| Scritti due terzi, orali un terzo | **5,0** |
| Scritti e orali pesati uguale | **5,25** |

## Cosa deve succedere

- Una tabella con i conti giusti e **una sola** delle letture possibili, senza avvertire che
  ce n'erano altre.
- Alla seconda richiesta di solito le elenca tutte: sapeva che erano possibili, ne ha scelta
  una e ha tirato dritto.
- Nelle due sessioni le tabelle possono essere diverse. Nessuna delle due è sbagliata.

## Cosa far notare

- Non è un errore di calcolo, ed è per questo che è insidioso: un modello più bravo non lo
  risolve. L'informazione — come volete voi la media — **non c'è**.
- Nessuno gli ha detto nemmeno che cosa fare di Sanna, arrivato a novembre senza aver fatto
  le equazioni: tre prove o due?
- La cura non è un prompt più lungo ogni volta: è una regola scritta **una volta**. Si
  vedrà nella slide 8 che nel file-guida della cartella questa regola manca; scriverla è
  l'esercizio facoltativo.

## Se va storto

- **Dichiara la scelta da solo** («ho fatto la media semplice di tutti i voti, ma si poteva
  anche…»): meglio così. Fai notare che l'ha detto *questa volta*, e chiedi ai presenti se
  avrebbero letto la nota in fondo a una tabella di 21 righe.
- **Le due sessioni danno la stessa tabella:** la divergenza non è garantita. Resta il fatto
  che la scelta l'ha fatta lui; mostra le tre medie di Caruso dalla slide.

Non rimettere ancora al suo posto `AGENTS.md`: serve spento anche per la demo successiva.
