# Ora 7 · Demo — La skill btc-task all'opera

> Conduce il formatore · circa 4 minuti · slide 5 di `slides/lezione-07.html`

## Prima della lezione

- [ ] Una copia pulita di `cartella-di-prova/`, aperta nell'agente, con `AGENTS.md` al suo
      posto.
- [ ] **La skill già installata** nella cartella di prova, con la richiesta dell'ora 6:

  ```
  Installa come skill di questo progetto quella che trovi qui:
  https://github.com/mporfido/skills/tree/main/teaching/btc-task
  Scarica SKILL.md. Poi dimmi in quale cartella l'hai messo.
  ```

  La cartella contiene un solo file, `SKILL.md` (circa 500 parole). Deve finire in
  `.claude/skills/btc-task/` con Claude Code, in `.agents/skills/btc-task/` con Codex e
  Antigravity.
- [ ] Una **prova il giorno prima**, per avere un'uscita di riserva da mostrare se in aula
      la rete non va. Salvatela in un file fuori dalla cartella di prova.

## Passi

1. Apri `SKILL.md` e scorri in fretta i pezzi evidenziati nella slide 4: il confine
   («Stop there»), l'ipotesi dichiarata, i tre principi, il formato.
2. Sessione nuova. Incolla la richiesta.
3. Leggi l'uscita ad alta voce, fermandoti sulle tre domande della slide.

## La richiesta

```
Usa la skill btc-task. Argomento: dal grafico di una parabola all'insieme
delle soluzioni di una disequazione di secondo grado. Classe terza di un
istituto tecnico.
```

L'argomento viene da `03-verifiche/verifica-02-disequazioni.md`: nelle osservazioni del
docente, molti hanno studiato bene il segno e poi hanno scritto l'intervallo sbagliato.

## Che cosa deve succedere

- **Tre sezioni e basta**: l'argomento riformulato, l'aggancio, la sequenza di passi
  (tipicamente 5-10). Niente verifica, niente rubrica, niente compiti per casa.
- **In italiano**, anche se la skill è in inglese: lo dice la voce *Language*.
- **Nessuna domanda preliminare**: la skill dice di procedere con ipotesi ragionevoli se il
  docente dà solo l'argomento.

## Che cosa far notare

- **Il confine.** Se l'agente aggiunge una sezione in più, il confine non ha tenuto: è il
  difetto più comune delle skill senza divieti espliciti, e qui il divieto c'è.
- **Un passo, una modifica.** Prendete due passi consecutivi e chiedete alla sala che cosa
  è cambiato fra l'uno e l'altro. Se sono cambiate due cose, lo avete trovato voi, non la
  skill: è il giudizio del docente sul risultato.
- **Il quadro teorico non è spiegato.** La skill non dice che cos'è *Building Thinking
  Classrooms*: il modello lo conosce. Sceglie quali principi contano e li rende vincolanti.
  È il ponte verso la skill che i corsisti scriveranno: non devono insegnare Bloom
  all'agente, devono dirgli come usarlo.

## Se qualcosa va storto

- **Antigravity la attiva anche senza nominarla**: lì `disable-model-invocation` non
  esiste. Non cambia niente per la demo, perché la skill la chiamate per nome comunque.
- **L'agente non la trova**: chiedigli «quali skill hai a disposizione in questo
  progetto?». Se non compare, ricontrolla la cartella di installazione.
- **Niente rete in aula**: mostra l'uscita salvata il giorno prima.
