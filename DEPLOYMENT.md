# 🚀 Deployment-Anleitung für GitHub Pages

## Schritt-für-Schritt-Anleitung

### 1. GitHub Repository erstellen

1. Gehe zu [GitHub](https://github.com) und logge dich ein
2. Klicke auf das **+** Symbol oben rechts → **New repository**
3. Repository-Name: `EndlessScroll` (oder ein anderer Name)
4. Beschreibung: `EndlessScroll Premium - Satirische Landing Page für Prokrastinations-App`
5. Wähle **Public** (für GitHub Pages erforderlich)
6. **NICHT** "Initialize with README" ankreuzen (wir haben bereits eines)
7. Klicke auf **Create repository**

---

### 2. Lokale Dateien zu GitHub hochladen

**Option A: Via GitHub Web Interface (einfachste Methode)**

1. Öffne dein neues Repository auf GitHub
2. Klicke auf **uploading an existing file**
3. Ziehe alle Dateien aus dem `EndlessScroll_Website` Ordner in das Upload-Feld:
   - `index.html`
   - `README.md`
   - `DEPLOYMENT.md`
   - `.gitignore`
   - Ordner `css/` (mit `style.css`)
   - Ordner `js/` (mit `script.js`)
   - Ordner `images/` (mit allen 3 Mockups)
4. Commit-Nachricht: `Initial commit: EndlessScroll Premium Landing Page`
5. Klicke auf **Commit changes**

**Option B: Via Git Command Line**

```bash
# In deinem lokalen EndlessScroll_Website Ordner
git remote add origin https://github.com/DEIN-USERNAME/EndlessScroll.git
git branch -M main
git push -u origin main
```

---

### 3. GitHub Pages aktivieren

1. Gehe zu deinem Repository auf GitHub
2. Klicke auf **Settings** (Zahnrad-Symbol)
3. Scrolle im linken Menü zu **Pages**
4. Unter **Source**:
   - Branch: Wähle `main` (oder `master`)
   - Folder: Wähle `/ (root)`
5. Klicke auf **Save**
6. Warte 1-2 Minuten

---

### 4. Deine Live-Website aufrufen

Nach dem Deployment erscheint oben auf der Pages-Seite ein grüner Banner:

```
Your site is live at https://DEIN-USERNAME.github.io/EndlessScroll/
```

**Das ist deine öffentliche URL!** 🎉

---

## 🔧 Änderungen vornehmen

### Dateien bearbeiten

1. **Direkt auf GitHub:**
   - Gehe zur Datei (z.B. `index.html`)
   - Klicke auf das Stift-Symbol (Edit)
   - Mache deine Änderungen
   - Scrolle nach unten und klicke **Commit changes**
   - GitHub Pages aktualisiert automatisch (dauert 1-2 Minuten)

2. **Lokal bearbeiten und hochladen:**
   - Bearbeite die Dateien auf deinem Computer
   - Gehe zu deinem Repository auf GitHub
   - Klicke auf **Add file** → **Upload files**
   - Ziehe die geänderten Dateien rein
   - Commit und warten

---

## 📝 Wichtige Hinweise

### Custom Domain (Optional)

Falls du eine eigene Domain hast:

1. In den **Pages-Einstellungen**
2. Unter **Custom domain** deine Domain eingeben (z.B. `endlessscroll.deine-domain.de`)
3. DNS-Einstellungen bei deinem Domain-Provider:
   - CNAME-Record: `endlessscroll` → `DEIN-USERNAME.github.io`
4. Warte auf DNS-Propagierung (kann bis zu 24h dauern)

### HTTPS aktivieren

- GitHub Pages aktiviert automatisch HTTPS
- Stelle sicher, dass **Enforce HTTPS** aktiviert ist (in Pages-Einstellungen)

### Bilder optimieren

Die Mockup-Bilder sind relativ groß (~2MB pro Bild). Für bessere Performance:

1. Bilder komprimieren mit [TinyPNG](https://tinypng.com)
2. Optimierte Versionen hochladen
3. Oder WebP-Format verwenden

---

## 🐛 Troubleshooting

### Website zeigt 404-Fehler

- Warte 2-3 Minuten nach dem ersten Deployment
- Prüfe, ob `index.html` im Root-Verzeichnis liegt
- Prüfe, ob GitHub Pages aktiviert ist

### Bilder werden nicht angezeigt

- Prüfe die Pfade in `index.html`:
  - `images/mockup_infinite_scroll.png` (relativ)
  - NICHT `/images/...` (absolut)
- Stelle sicher, dass alle Bilder hochgeladen wurden

### CSS/JS funktioniert nicht

- Prüfe die Pfade:
  - `css/style.css`
  - `js/script.js`
- Browser-Cache leeren (Strg+F5 / Cmd+Shift+R)

### Änderungen werden nicht angezeigt

- Warte 1-2 Minuten nach dem Commit
- Browser-Cache leeren
- Inkognito-Modus testen

---

## 📊 Analytics (Optional)

### Google Analytics hinzufügen

1. Erstelle ein Google Analytics Property
2. Kopiere den Tracking-Code
3. Füge ihn vor dem `</head>` in `index.html` ein:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

---

## ✅ Checkliste nach Deployment

- [ ] Website ist unter GitHub Pages URL erreichbar
- [ ] Alle Bilder werden korrekt angezeigt
- [ ] Navigation funktioniert (Smooth Scrolling)
- [ ] FAQ-Accordion funktioniert
- [ ] Buttons sind klickbar
- [ ] Responsive Design auf Handy getestet
- [ ] README.md mit Live-URL aktualisiert

---

## 🎉 Fertig!

Deine EndlessScroll Premium Landing Page ist jetzt live!

**Nächste Schritte:**
1. Teile die URL in deinem Portfolio
2. Verlinke sie auf bairytale.com
3. Teile sie in Social Media
4. Nutze sie als Referenz für Copywriting-Projekte

---

**Bei Fragen oder Problemen:** Siehe [GitHub Pages Dokumentation](https://docs.github.com/en/pages)
