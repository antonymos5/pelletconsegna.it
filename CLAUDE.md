# CLAUDE.md — pelletconsegna.it

## Descrizione e scopo

Sito dedicato alla **consegna di pellet a domicilio** a Lodi e provincia. Offre pellet certificato ENplus A1, consegna rapida, prezzi competitivi. Rivolto a privati e aziende con stufe a pellet nella zona del Lodigiano.  
Sito HTML/CSS statico con pagine geo-specifiche per singolo comune, pubblicato via GitHub Pages.

**Dominio:** https://www.pelletconsegna.it  
**Repository:** https://github.com/antonymos5/pelletconsegna.it

---

## Brand

- **Azienda:** Verde Oliva S.r.l.s.
- **P.IVA:** IT10927440965
- **Telefono:** 333 645 3219
- **Indirizzo:** Via Colombera 2, 26831 Casalmaiocco (LO)
- **Prodotto:** Pellet ENplus A1 certificato

---

## Struttura cartelle

```
pelletconsegna.it/
├── index.html                         # Homepage principale
├── privacy.html                       # Privacy policy
├── cookie.html                        # Cookie policy
├── robots.txt                         # Direttive crawler
├── sitemap.xml                        # Mappa del sito
├── og-image.png                       # Open Graph image
├── google2a5f68fcbab4234d.html        # Verifica Google Search Console
├── CNAME                              # Dominio custom GitHub Pages
├── blog/                              # Sezione blog editoriale
│   ├── index.html
│   └── quanto-costa-pellet-enplus-a1-2025.html
├── pellet-lodi.html                   # Pagine geo (flat files per comune)
├── pellet-casalmaiocco.html
├── pellet-sant-angelo-lodigiano.html
├── pellet-codogno.html
├── pellet-[comune].html               # ~60 pagine geo totali
└── ...
```

**Nota struttura:** A differenza degli altri siti, le pagine comunali sono **file HTML piatti** nella root (es. `pellet-lodi.html`), non cartelle.

---

## Zone geografiche target

Lodi (capoluogo), **Casalmaiocco** (sede operativa), e tutto il **Lodigiano**:  
Sant'Angelo Lodigiano, Codogno, Lodi Vecchio, San Martino in Strada, Tavazzano con Villavesco, Sordio, Massalengo, Marudo, Livraga, Brembio, Graffignana, San Colombano al Lambro, Secugnago, Turano Lodigiano, Valera Fratta, Borghetto Lodigiano, più comuni del milanese limitrofo.

---

## Regole SEO specifiche

### Keyword primari
- Homepage: `pellet consegna domicilio Lodi`, `acquistare pellet Lodi`
- Pagine geo: `pellet [comune]`, `consegna pellet [comune]`, `acquisto pellet [comune]`
- Long-tail: `pellet ENplus A1 Lodi`, `prezzo pellet 2025 Lodi`, `pellet a domicilio Lodigiano`

### Homepage
- H1: deve contenere "consegna pellet" + zona geografica.
- Evidenziare: certificazione ENplus A1, consegna rapida, prezzo al bancale/sacco.
- Schema.org: `LocalBusiness` + `Product` (pellet ENplus A1).
- Open Graph: usare `og-image.png` già presente.

### Pagine geo (pellet-[comune].html)
- `<title>`: `Pellet [Comune] | Consegna a Domicilio ENplus A1 – 333 645 3219`
- `<meta name="description">`: comune, ENplus A1, consegna rapida, prezzo, telefono.
- Canonical: `<link rel="canonical" href="https://www.pelletconsegna.it/pellet-[comune].html"/>`
- URL slug: formato `pellet-[nome-comune].html` (già esistente — non cambiare struttura).
- Schema.org: `LocalBusiness` + `Service` con `areaServed` = comune.
- H1: `Pellet a [Comune] – Consegna a Domicilio`
- Ogni pagina deve avere almeno 120 parole di contenuto unico oltre al template.

### Blog
- URL: `/blog/[slug].html`
- Keyword long-tail: "quanto costa pellet ENplus A1 2025", "differenza pellet A1 A2".
- Schema: `Article` + interlink verso pagine geo.

### Regole generali
- Citare sempre la certificazione **ENplus A1** — è il differenziante qualitativo chiave.
- `sitemap.xml`: includere tutte le pagine `pellet-[comune].html` + blog.
- `robots.txt`: `Allow: /`.
- Immagini: `alt` con "pellet ENplus A1 [comune]". Usare WebP.
- Interlink: ogni pagina geo → homepage + almeno 2 pagine geo vicine geograficamente.
- Non duplicare content: variare nome comune, distanza da Casalmaiocco, tempi di consegna stimati.

---

## Workflow GitHub

```bash
# Staging delle modifiche
git add <file>
# oppure
git add .

# Commit con messaggio descrittivo
git commit -m "descrizione della modifica"

# Pubblicazione
git push origin main
```

**Convenzioni commit:**
- `feat: aggiungi pagina pellet-[comune]`
- `fix: correggi canonical [comune]`
- `seo: aggiorna meta description homepage`
- `blog: aggiungi articolo [titolo]`
- `price: aggiorna prezzi pellet stagione 2025`

---

## Note operative

- Il sito è su **GitHub Pages** — push su `main` pubblica automaticamente.
- Le pagine geo sono **file piatti** nella root (es. `pellet-lodi.html`) — non usare cartelle per i comuni.
- Il numero **333 645 3219** sempre cliccabile: `<a href="tel:+393336453219">`.
- `og-image.png` è l'immagine Open Graph — usarla in tutti i tag `og:image`.
- Non eliminare `google2a5f68fcbab4234d.html` (verifica Search Console).
- Aggiornare i prezzi stagionalmente (autunno = picco domanda pellet).
