# Deployment-Anleitung für die AI Heat Systems Landing Page

## Übersicht

Die Website ist bereits auf GitHub hochgeladen und kann über verschiedene Hosting-Dienste dauerhaft bereitgestellt werden. Hier sind die einfachsten Optionen:

## GitHub Repository

**Repository URL:** https://github.com/Kevin180791/ai-heat-systems-landing

Das Repository ist öffentlich und enthält alle notwendigen Dateien für das Deployment.

---

## Option 1: GitHub Pages (Empfohlen - Kostenlos)

GitHub Pages ist die einfachste und kostenlose Lösung für statische Websites.

### Schritte:

1. Gehen Sie zu: https://github.com/Kevin180791/ai-heat-systems-landing
2. Klicken Sie auf **Settings** (Einstellungen)
3. Scrollen Sie im linken Menü zu **Pages**
4. Unter **Source** wählen Sie:
   - Branch: `main`
   - Folder: `/ (root)`
5. Klicken Sie auf **Save**
6. Nach 1-2 Minuten ist die Website verfügbar unter:
   - `https://kevin180791.github.io/ai-heat-systems-landing/`

### Vorteile:
- ✅ Kostenlos
- ✅ Automatische Updates bei Git-Push
- ✅ HTTPS inklusive
- ✅ Keine Konfiguration nötig

---

## Option 2: Netlify (Empfohlen - Kostenlos + Mehr Features)

Netlify bietet mehr Features wie Custom Domains, Form-Handling und bessere Performance.

### Schritte:

1. Gehen Sie zu: https://www.netlify.com/
2. Klicken Sie auf **Sign up** (oder **Log in** falls Sie bereits einen Account haben)
3. Wählen Sie **Import from Git**
4. Verbinden Sie Ihr GitHub-Konto
5. Wählen Sie das Repository: `Kevin180791/ai-heat-systems-landing`
6. Build-Einstellungen:
   - Build command: (leer lassen)
   - Publish directory: `.` (Punkt)
7. Klicken Sie auf **Deploy site**
8. Nach 1-2 Minuten erhalten Sie eine URL wie:
   - `https://ai-heat-systems.netlify.app/`
9. Optional: Custom Domain hinzufügen unter **Domain settings**

### Vorteile:
- ✅ Kostenlos (für statische Sites)
- ✅ Automatische Deployments bei Git-Push
- ✅ HTTPS inklusive
- ✅ Custom Domains möglich
- ✅ Bessere Performance (CDN)
- ✅ Form-Handling
- ✅ Analytics verfügbar

---

## Option 3: Vercel (Alternative zu Netlify)

Vercel ist ähnlich wie Netlify und ebenfalls sehr einfach zu nutzen.

### Schritte:

1. Gehen Sie zu: https://vercel.com/
2. Klicken Sie auf **Sign up** mit GitHub
3. Klicken Sie auf **New Project**
4. Wählen Sie das Repository: `Kevin180791/ai-heat-systems-landing`
5. Klicken Sie auf **Deploy**
6. Nach 1-2 Minuten erhalten Sie eine URL wie:
   - `https://ai-heat-systems.vercel.app/`

### Vorteile:
- ✅ Kostenlos (für statische Sites)
- ✅ Automatische Deployments
- ✅ HTTPS inklusive
- ✅ Custom Domains möglich
- ✅ Sehr schnelle Performance

---

## Option 4: Cloudflare Pages (Kostenlos + Schnell)

Cloudflare Pages bietet hervorragende Performance durch das globale CDN.

### Schritte:

1. Gehen Sie zu: https://pages.cloudflare.com/
2. Melden Sie sich an oder erstellen Sie einen Account
3. Klicken Sie auf **Create a project**
4. Verbinden Sie Ihr GitHub-Konto
5. Wählen Sie das Repository: `Kevin180791/ai-heat-systems-landing`
6. Build-Einstellungen:
   - Build command: (leer lassen)
   - Build output directory: `/`
7. Klicken Sie auf **Save and Deploy**
8. Nach 1-2 Minuten ist die Website live

### Vorteile:
- ✅ Kostenlos (unbegrenzt)
- ✅ Extrem schnelles CDN
- ✅ HTTPS inklusive
- ✅ Custom Domains möglich
- ✅ DDoS-Schutz inklusive

---

## Option 5: Eigener Server (Für volle Kontrolle)

Falls Sie einen eigenen Webserver haben (z.B. bei einem Hosting-Provider):

### Via FTP/SFTP:

1. Laden Sie das ZIP-Archiv herunter
2. Entpacken Sie es lokal
3. Verbinden Sie sich per FTP/SFTP mit Ihrem Server
4. Laden Sie alle Dateien aus dem `ai-heat-landing/` Ordner hoch
5. Die Website ist sofort verfügbar unter Ihrer Domain

### Via SSH/Git:

```bash
# Auf dem Server
cd /var/www/html/
git clone https://github.com/Kevin180791/ai-heat-systems-landing.git
cd ai-heat-systems-landing

# Optional: Webserver-Konfiguration (z.B. für Apache)
# Erstellen Sie eine .htaccess für saubere URLs
```

---

## Empfehlung

**Für maximale Einfachheit:** GitHub Pages
**Für beste Features:** Netlify
**Für beste Performance:** Cloudflare Pages

Alle drei Optionen sind kostenlos und bieten automatische Updates, wenn Sie Änderungen am GitHub-Repository vornehmen.

---

## Custom Domain einrichten

Falls Sie eine eigene Domain haben (z.B. `ai-heat-systems.com`):

### Bei GitHub Pages:
1. Fügen Sie eine `CNAME` Datei im Repository hinzu mit Ihrer Domain
2. Konfigurieren Sie DNS bei Ihrem Domain-Provider:
   - A-Record: `185.199.108.153`
   - A-Record: `185.199.109.153`
   - A-Record: `185.199.110.153`
   - A-Record: `185.199.111.153`

### Bei Netlify/Vercel/Cloudflare:
1. Gehen Sie zu den Domain-Einstellungen in Ihrem Dashboard
2. Fügen Sie Ihre Custom Domain hinzu
3. Folgen Sie den Anweisungen für DNS-Konfiguration
4. HTTPS wird automatisch konfiguriert

---

## Updates vornehmen

Wenn Sie Änderungen an der Website vornehmen möchten:

```bash
# Lokal Änderungen vornehmen
cd ai-heat-landing
# Dateien bearbeiten...

# Änderungen committen und pushen
git add .
git commit -m "Update: Beschreibung der Änderung"
git push origin main
```

Die Website wird automatisch aktualisiert (bei GitHub Pages, Netlify, Vercel, Cloudflare).

---

## Support & Troubleshooting

### Website lädt nicht:
- Warten Sie 2-3 Minuten nach dem Deployment
- Leeren Sie den Browser-Cache (Strg+F5)
- Überprüfen Sie die Deployment-Logs im jeweiligen Dashboard

### Video spielt nicht ab:
- Überprüfen Sie, ob die Datei `assets/videos/final_video.mp4` vorhanden ist
- Stellen Sie sicher, dass der Browser HTML5 Video unterstützt
- Prüfen Sie die Browser-Konsole auf Fehler (F12)

### Downloads funktionieren nicht:
- Stellen Sie sicher, dass alle Dateien im `assets/docs/` Ordner vorhanden sind
- Überprüfen Sie die Dateipfade in `index.html`

---

## Kontakt

Bei Fragen zum Deployment oder technischen Problemen:
- GitHub Issues: https://github.com/Kevin180791/ai-heat-systems-landing/issues
- Repository: https://github.com/Kevin180791/ai-heat-systems-landing

---

**Viel Erfolg mit Ihrer Landing Page! 🚀**

