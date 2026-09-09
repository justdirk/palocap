# Palocap — sito

Sito statico per **Palocap**, abbigliamento personalizzato a Milano dal 1998.
Ricamo, stampa e dipinto a mano. Corso di Porta Ticinese 1 e Piazza Piemonte 10.

## Struttura

```
index.html        pagina unica in italiano, HTML + CSS inline, nessun build
en/index.html     la stessa pagina in inglese (stesso CSS, stesse immagini via ../assets/)
assets/           immagini (WebP) e logo (PNG con trasparenza)
robots.txt        aperto a tutti, con i crawler AI elencati esplicitamente
sitemap.xml       le due pagine con le alternative hreflang
llms.txt          scheda in testo semplice per gli assistenti AI (chi siamo, cosa facciamo, dove, orari)
```

Nessuna dipendenza da installare. Gli unici file esterni sono i caratteri
(Google Fonts: Archivo e Martian Mono).

## Versione inglese

`/en/` è una traduzione completa, non un toggle JavaScript: pagina separata, `lang="en"`,
title/description/JSON-LD in inglese, `hreflang` incrociato fra le due versioni e
selettore IT/EN nella barra di navigazione. Le due pagine condividono CSS e immagini, quindi
**ogni modifica di layout va fatta in entrambi i file** (il testo è l'unica differenza).

A chi serve: turisti, studenti internazionali (Bocconi, Politecnico, NABA, IED), team aziendali
stranieri, chi è in città per Fashion Week / Salone. Le recensioni Google sono tradotte e
dichiarate come tali. Il numero di telefono è in formato internazionale (+39).

## Pubblicazione

GitHub Pages, da `main` / root → https://justdirk.github.io/palocap/

## Contenuti

- Logo storico recuperato dall'archivio del vecchio sito, ripulito e reso trasparente
- Sezione **Archivio**: i modelli disegnati e prodotti da Palocap fra il 2004 e il 2007,
  con i codici originali (ART. 99, ART. 981, ART. 07)
- Fotografie: campagne d'archivio anni Duemila + scatti recenti da Instagram
- Modulo preventivo: compone un'email precompilata, nessun backend richiesto

## Da completare

- **Numero WhatsApp** — segnaposto in rosso nella sezione Preventivo
- **Ragione sociale e partita IVA** nel footer, obbligatorie per legge su un sito aziendale italiano
- **Fotografia**: servirebbe un servizio dedicato — macchina da ricamo in funzione,
  primo piano del ricamo sul tessuto, pennello, coni di filo, interno negozio, ritratto al banco

## Segnaposto da sostituire

Il numero WhatsApp è un segnaposto: cerca `39XXXXXXXXXX` in `index.html` e
sostituiscilo col numero vero (formato internazionale senza + e senza spazi,
es. `393491144622`). Finché resta il segnaposto, tutti i pulsanti WhatsApp
si nascondono da soli — il sito non mostra mai un link rotto.

Restano inoltre da confermare, segnati in rosso nella pagina:

- tempi di consegna (FAQ)
- spedizioni fuori Milano (FAQ)
- ragione sociale e partita IVA (footer)

## SEO

Fatto: title e description mirati su «ricamo / magliette personalizzate Milano»,
H1 con la riga di servizio, dati strutturati JSON-LD (Organization, due
ClothingStore con indirizzi e orari, FAQPage), `robots.txt`, `sitemap.xml`,
alt text su tutte le immagini, `width`/`height` e `loading="lazy"`.

Da completare quando il dominio è deciso:

- `<link rel="canonical">` nella head
- `og:image` con URL assoluto
- gli URL in `robots.txt`, `sitemap.xml`, `llms.txt` e nei tag `hreflang` (ora puntano a www.palocap.com)

## Farsi consigliare dagli assistenti AI (ChatGPT, Gemini, Perplexity, Copilot)

Gli assistenti non hanno un indice proprio: ChatGPT e Copilot cercano su **Bing**, Gemini e le
AI Overview su **Google**, Perplexity su un mix di entrambi più siti di recensioni. Poi filtrano
per schede locali, recensioni recenti e liste «migliori a Milano». Quindi, in ordine di resa:

1. **Bing Places for Business** (bingplaces.com) — la scheda locale di Bing. Si importa da Google
   Business Profile in 10 minuti. Senza questa ChatGPT non «vede» il negozio come attività locale.
2. **Bing Webmaster Tools** (bing.com/webmasters) — verifica del sito, invio della sitemap.
   Si può importare direttamente da Google Search Console.
3. **Google Search Console** — verifica + sitemap, se non è già fatto.
4. **Google Business Profile** — tenere aggiornati orari, foto e categoria («Negozio di ricami» /
   «Stampa su magliette»); chiedere recensioni con costanza: per le AI la recenza conta quanto il numero.
5. **Apple Business Connect** (businessconnect.apple.com) — Apple Maps / Siri; gratuito.
6. **Menzioni di terzi** — è il segnale più forte: Yelp, TripAdvisor, PagineGialle, guide
   «dove fare magliette personalizzate a Milano», r/milano. Le AI citano chi viene citato.
7. **Nome, indirizzo e telefono identici** su tutte le schede (NAP consistency).

Sul sito è già fatto: dati strutturati LocalBusiness/FAQ, `robots.txt` che ammette
esplicitamente GPTBot, ClaudeBot, PerplexityBot ecc., `llms.txt`, pagina inglese.
Tutto questo però vale solo quando il sito è raggiungibile sul suo dominio: finché
palocap.com serve il vecchio sito Flash, i motori indicizzano quello.

Nota: la valutazione Google è mostrata in pagina ma **non** è marcata nei dati
strutturati. Le linee guida di Google vietano di marcare come proprie le
recensioni raccolte da terzi: farlo rischia un'azione manuale.
