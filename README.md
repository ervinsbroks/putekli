# Putekļi — testa leibla lapa

Vienkārša statiska lapa (HTML + CSS, bez build soļiem), ko var publicēt ar GitHub Pages.

## Failu struktūra

```
putekli-label/
├── index.html
├── README.md
├── .nojekyll
└── assets/
    └── covers/
        ├── cover-1.jpg
        ├── cover-2.jpg
        ├── cover-3.jpg
        ├── cover-4.jpg
        └── cover-5.jpg
```

`index.html` jābūt repozitorija saknē, citādi GitHub Pages to neatradīs.

## Publicēšana GitHub

### 1. Izveido repozitoriju
1. Atver https://github.com/new
2. Nosaukums, piemēram, `putekli-label`.
3. Izvēlies **Public**.
4. Neliec ķeksīšus pie README, .gitignore vai licences (faili jau ir).
5. Spied **Create repository**.

### 2A. Augšupielāde pārlūkā (bez Git)
1. Repozitorija lapā spied **uploading an existing file**.
2. Velc iekšā visus failus un mapi `assets` (izvelc ZIP arhīvu un velc saturu, nevis pašu ZIP).
3. Spied **Commit changes**.

### 2B. Augšupielāde ar Git
```bash
cd putekli-label
git init
git add .
git commit -m "Pirmā versija"
git branch -M main
git remote add origin https://github.com/TAVS-LIETOTAJVARDS/putekli-label.git
git push -u origin main
```

### 3. Ieslēdz GitHub Pages
1. Repozitorijā atver **Settings → Pages**.
2. Sadaļā **Build and deployment** izvēlies **Source: Deploy from a branch**.
3. Branch: `main`, mape: `/ (root)`. Spied **Save**.
4. Pēc 1–2 minūtēm lapa būs adresē:
   `https://TAVS-LIETOTAJVARDS.github.io/putekli-label/`

### 4. Atjauninājumi
Izmaini failus, tad `git add . && git commit -m "Izmaiņas" && git push`. Pages atjaunojas pats.

## Ja kaut kas nestrādā
- **404**: pārbaudi, vai `index.html` ir saknē, nevis apakšmapē.
- **Nav bilžu**: faila nosaukumi ir reģistrjutīgi (`cover-1.jpg`, nevis `Cover-1.JPG`).
- **Vecs saturs**: pārlādē ar Ctrl/Cmd + Shift + R.

## Pielāgošana
- Krāsas: `:root` bloks `index.html` sākumā.
- Izdevumi: sadaļa `#izdevumi`, viens `<li class="release">` katram.
- Kontakta e-pasts: `mailto:` saite sadaļā `#kontakti`.
