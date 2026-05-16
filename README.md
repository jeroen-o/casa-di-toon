# 🏡 La Casa di Toon

Statische website voor een vakantiehuis in Bagni di Lucca, Toscane. Eén HTML-pagina, geen build-stap, klaar om te deployen op GitHub Pages of elke andere statische host.

## 🚀 Deploy op GitHub Pages (in 5 minuten)

### Optie A — Via web (geen Git-kennis nodig)

1. Maak een GitHub-account aan op [github.com](https://github.com) (als je er nog geen hebt).
2. Klik rechtsboven op **+** → **New repository**.
3. **Repository name**: `casa-di-toon` (of een andere naam — schrijf 'm op).
4. Vink **Public** aan en klik **Create repository**.
5. Klik op **uploading an existing file** in de quick-setup tekst.
6. Sleep alle bestanden uit deze map (inclusief de `images/` submap) naar het venster.
7. Klik **Commit changes**.
8. Ga naar **Settings** → **Pages** (linker zijbalk).
9. Bij **Source**: kies **Deploy from a branch**, branch **main**, folder **/ (root)**.
10. Klik **Save**.

Na 1–2 minuten staat de site op:
```
https://<JOUW-GEBRUIKERSNAAM>.github.io/casa-di-toon/
```

### Optie B — Via Git CLI

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin git@github.com:<USERNAME>/casa-di-toon.git
git push -u origin main
```
Daarna in GitHub → Settings → Pages → Source: main / root.

## 🌐 Eigen domeinnaam (optioneel)

1. Koop een domein (bijv. `lacasaditoon.nl` of `casaditoon.com`).
2. Bij je domein-provider voeg DNS-records toe:
   - `A` records naar `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Of een `CNAME` naar `<USERNAME>.github.io`
3. Maak een bestand `CNAME` (geen extensie) in de root met daarin: `lacasaditoon.nl`
4. In GitHub → Settings → Pages → Custom domain: vul het domein in en vink **Enforce HTTPS** aan.

## ⚙️ Aanpassen voor jouw URL

Doe één keer een **zoek-en-vervang** in alle bestanden (`index.html`, `404.html`, `robots.txt`, `sitemap.xml`, `llms.txt`, `manifest.webmanifest`):

| Vervang dit                                | Door dit                                              |
|--------------------------------------------|-------------------------------------------------------|
| `https://casa-di-toon.example.com`         | jouw definitieve URL (zonder slash op het eind)       |

In VS Code: **Ctrl+Shift+H** (Windows) of **Cmd+Shift+H** (Mac).

## 📂 Wat zit er in de map?

```
.
├── index.html              ← de website
├── 404.html                ← foutpagina
├── favicon.svg             ← icoontje in browser-tab
├── manifest.webmanifest    ← voor toevoegen aan startscherm op mobiel
├── robots.txt              ← instructies voor zoekmachines
├── sitemap.xml             ← sitemap voor Google etc.
├── llms.txt                ← GEO-bestand voor AI-assistenten
├── .nojekyll               ← uit Jekyll, in moderne deploy
└── images/
    ├── zwembad-1600.jpg    ← hero foto (desktop)
    ├── zwembad-800.jpg     ← hero foto (mobiel)
    ├── huis-1200.jpg
    ├── huis-600.jpg
    ├── woonkamer-1600.jpg
    ├── woonkamer-800.jpg
    ├── og-image.jpg        ← preview bij delen op social media
    └── apple-touch-icon.jpg
```

## 🔍 SEO en GEO

De site is geoptimaliseerd voor:

- **Klassieke SEO**: meta-tags, semantic HTML, sitemap, robots.txt, hreflang, geo-meta, canonical URL
- **Social sharing**: Open Graph + Twitter Card met preview-foto
- **Structured data**: JSON-LD voor `LodgingBusiness`, `VacationRental`, `FAQPage`, `BreadcrumbList`
- **GEO (Generative Engine Optimization)**: `llms.txt`, FAQ-sectie met heldere Q&A, semantische entity-koppelingen, expliciete user-agent toegang voor GPTBot, ClaudeBot, PerplexityBot etc.
- **Performance**: preconnect fonts, preload hero, responsive `srcset` images, lazy loading
- **Mobile-first**: getest op viewports vanaf 320px breed, touch targets minimaal 44px

## 🛠️ Lokaal testen

Open `index.html` in je browser. Voor wat realistischer testen (sommige features vereisen een server):

```bash
# Python (al geïnstalleerd op Mac/Linux)
python3 -m http.server 8000

# Daarna in browser: http://localhost:8000
```

## 📞 Boekingen

Alle WhatsApp-knoppen verwijzen naar **+31 6 11 77 39 13**. Wil je dit aanpassen? Zoek-en-vervang `31611773913` (zonder spaties en plus-teken) in `index.html`.

---

Gebouwd met een dosis Italiaanse zon ☀️
