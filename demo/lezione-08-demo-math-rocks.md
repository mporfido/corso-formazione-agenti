# Lezione 8 · Demo — La stessa lezione, vista da due parti

> Conduce il formatore · circa 10 minuti · slide 3 di `slides/lezione-08.html`

Non c'è niente da far eseguire all'agente: si guarda una lezione vera dalla parte dello
studente e, accanto, il file di testo da cui nasce. Il messaggio è uno solo: **il file dice
che cosa mostrare, il motore sa come farlo funzionare.**

## Prima della lezione

- [ ] Due finestre affiancate:
  - nel browser, il sito pubblicato di math-rocks: <https://mporfido.github.io/math-rocks/>;
  - in un editor di testo (o nel pannello file dell'agente), la cartella `content/` di
    math-rocks, in `C:\Users\mikil\Documents\Repository\math-rocks`.
- [ ] Aperti e provati, in questo ordine:
  1. *Le frazioni come aree*: `content/le-frazioni/content-1.md`. Ha domande a scelta
     multipla, e il contenuto che si rivela dopo le risposte;
  2. *La funzione esponenziale*, primo passo («La scala delle potenze»):
     `content/funzione-esponenziale/content-1.md`. Ha uno slider legato al testo;
  3. un passo con un'animazione: `content/introduzione-alle-funzioni/content-1.md` o
     `content/equazioni-lineari/content-1.md`.
- [ ] Una **riserva** se la rete non va: un'esecuzione locale di math-rocks, oppure tre
      screenshot dei passi sopra. Per l'anteprima locale si usa `python app.py` da quella
      cartella, con le dipendenze installate.
- [ ] Il file `README.md` di Geode aperto in un'altra scheda, per la slide successiva.

## Passi

1. **Lo studente.** Nel browser apri *Le frazioni*. Rispondi a una domanda sbagliando
   apposta: lo studente vede il feedback. Rispondi giusto: il passo si sblocca.
2. **Chi scrive.** Apri `content/le-frazioni/content-1.md`. Fai trovare ai corsisti la
   domanda appena fatta: è un paragrafo con le risposte fra doppie parentesi quadre e un
   asterisco davanti a quella giusta. Non spiegare la sintassi: mostra che è testo.
3. **Lo slider.** Torna nel browser, apri *La funzione esponenziale*, muovi lo slider. Poi
   apri il file: lo slider è una riga di testo con un nome e tre numeri. Chiedi: «quando
   lo muovo, il file cambia?». No: dice che cosa mostrare, non come farlo funzionare.
4. **L'animazione.** Mostra un passo con un'animazione, e nel file il blocco che la
   contiene. Qui si dice una cosa sola: è un pezzo di programma che qualcuno ha scritto
   *dentro* il file, ed è l'unico punto in cui servirebbe sapere programmare.
5. **Il confine.** Apri l'esplora file di math-rocks. Indica a voce `content/` e
   `site.yaml` da una parte e `parser/`, `routes/` e `templates/` dall'altra: «le lezioni
   stanno qui; il motore sta là, e non lo apriamo mai». Il disegno della slide 4 dice la
   stessa cosa.

## Che cosa deve succedere

- Il passo dello studente e il file di testo si riconoscono: i corsisti ritrovano la loro
  risposta e le loro opzioni nel file.
- Qualcuno chiede «ma chi l'ha scritto?». Risposta onesta: math-rocks l'ha scritto
  l'autore, con l'aiuto di un agente e molta correzione a mano. È il metodo della lezione 8.

## Se qualcosa va storto

- **Il sito non si apre.** Piano B: screenshot, o la copia locale.
- **Un corsista chiede di vedere il motore.** Aprine un file, tre secondi, e richiudilo:
  si vede subito che è un'altra cosa. Torna alla slide.
- **Qualcuno chiede se serve saper programmare.** No: nel file di una lezione c'è testo.
  Il codice compare solo nelle animazioni, e la lezione 9 non le richiede.
