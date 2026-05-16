# 🏡 La Casa di Toon

Statische website voor het vakantiehuis in Bagni di Lucca, Toscane.
Live op **https://jeroen-o.github.io/casa-di-toon/** (na deploy via GitHub Pages).

## ✅ Wat is er klaar

- **Eén HTML-pagina**, geen build-stap, geen externe afhankelijkheden (behalve Google Fonts)
- **Mobile-first responsive**: getest vanaf 320px breed
- **Volledige SEO**: meta-tags, sitemap, hreflang, geo-meta, Open Graph, Twitter Card
- **GEO** (AI-vindbaarheid): `llms.txt`, FAQ-sectie, JSON-LD structured data, expliciete toegang voor GPTBot/ClaudeBot/PerplexityBot
- **Performance**: srcset responsive images, lazy loading, preconnect fonts, preload hero
- **Accessibility**: skip-link, semantic HTML5, ARIA-labels, `prefers-reduced-motion`
- **Alle paden zijn relatief**: werkt op `jeroen-o.github.io/casa-di-toon/` én later op een eigen domein zonder aanpassingen

## 🚀 Deployen

De bestanden zitten al op `github.com/jeroen-o/casa-di-toon`. Om de site live te zetten:

1. Open je repository op GitHub
2. Klik **Settings** (bovenin)
3. Klik **Pages** (linker zijbalk)
4. Onder **Source**: kies **Deploy from a branch** → **main** → **/ (root)** → **Save**
5. Wacht 1–2 minuten

Je site staat dan op:
```
https://jeroen-o.github.io/casa-di-toon/
```

## 🔍 Checks na deployment

Open in je browser (vervang als je een eigen domein gebruikt):

- ✅ https://jeroen-o.github.io/casa-di-toon/ → de site zelf
- ✅ https://jeroen-o.github.io/casa-di-toon/robots.txt → moet `Sitemap:` regel tonen
- ✅ https://jeroen-o.github.io/casa-di-toon/sitemap.xml → moet XML zijn met de juiste URLs
- ✅ https://jeroen-o.github.io/casa-di-toon/llms.txt → markdown voor AI-bots
- ✅ https://jeroen-o.github.io/casa-di-toon/iets-fouts → moet 404-pagina tonen

**Submit de sitemap aan zoekmachines:**
- Google Search Console → Sitemaps → `https://jeroen-o.github.io/casa-di-toon/sitemap.xml`
- Bing Webmaster Tools → Sitemaps → idem

**Test JSON-LD structured data:**
- https://search.google.com/test/rich-results → plak je URL in
- Should pass: `LodgingBusiness`, `FAQPage`, `WebSite`

## 🌐 Eigen domeinnaam (optioneel)

Stel je koopt `lacasaditoon.nl`:

1. Bij je domein-provider DNS records toevoegen:
   - **A** records naar:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - Óf één **CNAME** `www` naar `jeroen-o.github.io`
2. Maak een bestand `CNAME` (geen extensie) in de root met daarin: `lacasaditoon.nl`
3. In GitHub → Settings → Pages → **Custom domain**: vul het domein in → save
4. Vink **Enforce HTTPS** aan (komt automatisch beschikbaar na DNS-propagatie)

**Belangrijk:** na een custom domain moet je in alle bestanden de URL aanpassen:
- Zoek-en-vervang: `https://jeroen-o.github.io/casa-di-toon` → `https://lacasaditoon.nl`
- Bestanden waarin het voorkomt: `index.html`, `404.html`, `robots.txt`, `sitemap.xml`, `llms.txt`

DNS-propagatie duurt 5 minuten tot 24 uur, afhankelijk van je registrar.

## 📂 Bestanden

```
.
├── index.html              ← de website
├── 404.html                ← foutpagina
├── favicon.svg             ← browser-tab icoontje
├── manifest.webmanifest    ← voor "toevoegen aan startscherm" op mobiel
├── robots.txt              ← zoekmachine-instructies
├── sitemap.xml             ← sitemap voor Google
├── llms.txt                ← AI-instructies (GEO)
├── .nojekyll               ← GitHub Pages config
├── README.md               ← dit bestand
└── images/
    ├── zwembad-1600.jpg    ← hero foto (desktop)
    ├── zwembad-800.jpg     ← hero foto (mobiel)
    ├── huis-1200.jpg / huis-600.jpg
    ├── woonkamer-1600.jpg / woonkamer-800.jpg
    ├── og-image.jpg        ← social media preview
    └── apple-touch-icon.jpg
```

## 📞 Boekingen

Alle WhatsApp-knoppen verwijzen naar **+31 6 11 77 39 13**. Aanpassen? Zoek-en-vervang `31611773913` in `index.html`.

---

🍝
