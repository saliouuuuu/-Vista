# Vista — Landing page

Landing statica per **Vista**: video promozionali per host Airbnb &amp; B&amp;B, creati dalle foto che il cliente ha già.

Sito in HTML/CSS/JS puro, nessun build step. Hero a schermo intero con la casa che si anima in base allo scroll (parallax + pin), poi le sezioni: come funziona, esempio, recensioni, prezzi, FAQ, CTA WhatsApp.

## Struttura
- `index.html` — la landing completa (CSS e JS inline).
- `privacy.html`, `termini.html`, `cookie.html` — pagine legali (modelli base, linkate dal footer).
- `netlify.toml` — publish + header di sicurezza.
- `images/` — immagini ottimizzate per il web (hero, interni, gallery).

## Prima di pubblicare
1. **WhatsApp** — impostato su `+39 351 383 7210` (link `wa.me/393513837210` nella CTA finale). Per cambiarlo, modifica il numero in `index.html`.
2. **Dati legali** — in `privacy.html`, `termini.html`, `cookie.html` sostituisci i campi tra `[parentesi quadre]` (titolare, P.IVA, email, indirizzo, data). Aggiorna la P.IVA anche nel footer di `index.html` ("P.IVA da inserire").
3. **Immagini** (facoltativo) — sostituisci quelle in `images/` con foto tue mantenendo gli stessi nomi.

## Deploy su Netlify
```bash
npm install -g netlify-cli
netlify login
netlify deploy --dir=. --prod
```
Oppure drag &amp; drop della cartella su app.netlify.com.

## Note tecniche
- Nessuna dipendenza, nessun build.
- Font da Google Fonts (Space Grotesk + Archivo).
- `prefers-reduced-motion` rispettato, focus da tastiera visibile, responsive fino a mobile.
