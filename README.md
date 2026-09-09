# Palocap — sito

Sito statico per **Palocap**, abbigliamento personalizzato a Milano dal 1998.
Ricamo, stampa e dipinto a mano. Corso di Porta Ticinese 1 e Piazza Piemonte 10.

## Struttura

```
index.html        pagina unica, HTML + CSS inline, nessun build
assets/           immagini (WebP) e logo (PNG con trasparenza)
```

Nessuna dipendenza da installare. Gli unici file esterni sono i caratteri
(Google Fonts: Archivo e Martian Mono).

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
- gli URL in `robots.txt` e `sitemap.xml` (ora puntano a www.palocap.com)

Nota: la valutazione Google è mostrata in pagina ma **non** è marcata nei dati
strutturati. Le linee guida di Google vietano di marcare come proprie le
recensioni raccolte da terzi: farlo rischia un'azione manuale.
