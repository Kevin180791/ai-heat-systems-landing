# Dezentrale KI-Wärme-Systeme - Landing Page

## Übersicht

Diese Landing Page präsentiert das Konzept dezentraler KI-Wärme-Systeme – eine innovative Lösung, die KI-Hardware mit intelligenter Abwärmenutzung kombiniert.

## Features

### Interaktive Elemente
- **Video-Integration**: Eingebettetes Konzept-Video mit cinematic Animationen
- **Smooth Scrolling**: Flüssige Navigation zwischen Sektionen
- **Fade-in Animationen**: Elemente werden beim Scrollen animiert eingeblendet
- **Parallax-Effekte**: Subtile Bewegungseffekte für visuelles Interesse
- **Responsive Design**: Optimiert für Desktop, Tablet und Mobile

### Sektionen

1. **Hero Section**
   - Beeindruckender erster Eindruck mit 3D-Rendering
   - Call-to-Action Buttons
   - Animiertes Floating-Element

2. **Video Section**
   - Eingebettetes Konzept-Video (29 Sekunden)
   - Professionelle Präsentation der Vision

3. **Vision Section**
   - Vier Kernsäulen des Projekts
   - Interaktive Hover-Effekte

4. **Konzept Section**
   - Dual-Use-Modell Erklärung
   - Feature-Liste mit Icons

5. **Stats Section**
   - Animierte Zahlen
   - Marktdaten und ROI

6. **Downloads Section**
   - 6 Download-Karten für alle Materialien
   - Direktlinks zur Präsentation und Dokumenten

7. **CTA Section**
   - Abschließender Call-to-Action
   - Kernwerte-Badges

## Technologie-Stack

- **HTML5**: Semantisches Markup
- **CSS3**: Custom Properties, Grid, Flexbox, Animations
- **JavaScript**: Vanilla JS für Interaktivität
- **Font Awesome**: Icons
- **Google Fonts**: Montserrat & Roboto

## Farbschema

```css
--color-dark-primary: #1a1a2e
--color-dark-secondary: #16213e
--color-dark-tertiary: #0f3460
--color-accent: #00d4ff
--color-white: #ffffff
```

## Struktur

```
ai-heat-landing/
├── index.html              # Haupt-HTML-Datei
├── styles.css              # Stylesheet
├── script.js               # JavaScript-Funktionen
├── README.md               # Diese Datei
└── assets/
    ├── videos/
    │   └── final_video.mp4
    ├── docs/
    │   ├── final_report.md
    │   ├── prototyp_konzept_analyse.md
    │   ├── technical_concept_and_innovation.md
    │   └── brainstorming_and_structure.md
    └── images/
        ├── prototype_concept.png
        ├── system_integration.png
        ├── decentralized_network.png
        └── technology_roadmap.png
```

## Lokale Entwicklung

### Voraussetzungen
- Python 3 (für lokalen Server)
- Moderner Webbrowser

### Server starten

```bash
cd ai-heat-landing
python3 -m http.server 8080
```

Dann öffnen Sie `http://localhost:8080` im Browser.

## Deployment

Die Landing Page ist vollständig statisch und kann auf jedem Webserver gehostet werden:

- **GitHub Pages**: Einfach das Repository pushen und GitHub Pages aktivieren
- **Netlify**: Drag & Drop des Ordners
- **Vercel**: Git-Integration oder CLI-Upload
- **AWS S3**: Als statische Website konfigurieren
- **Traditioneller Webserver**: Dateien per FTP/SFTP hochladen

## Browser-Kompatibilität

- Chrome/Edge: ✅ Vollständig unterstützt
- Firefox: ✅ Vollständig unterstützt
- Safari: ✅ Vollständig unterstützt
- Mobile Browser: ✅ Responsive Design

## Performance

- **Ladezeit**: < 3 Sekunden (bei guter Verbindung)
- **Video-Größe**: ~7.4 MB (optimiert für Web)
- **Bilder**: PNG mit Kompression
- **CSS/JS**: Minimiert und optimiert

## Anpassungen

### Farben ändern
Bearbeiten Sie die CSS-Variablen in `styles.css`:

```css
:root {
    --color-accent: #00d4ff; /* Ihre Akzentfarbe */
}
```

### Inhalte aktualisieren
Bearbeiten Sie `index.html` und passen Sie Texte, Links und Bilder an.

### Neue Sektionen hinzufügen
Folgen Sie dem bestehenden Muster in `index.html` und fügen Sie entsprechende Styles in `styles.css` hinzu.

## Lizenz

Open Source - Frei verwendbar für das Projekt "Dezentrale KI-Wärme-Systeme"

## Kontakt

Für Fragen oder Anregungen zur Landing Page oder zum Projekt, nutzen Sie die Kontaktmöglichkeiten auf der Website.

---

**Erstellt mit**: HTML5, CSS3, JavaScript
**Design-Inspiration**: Moderne Tech-Startups, Cyberpunk-Ästhetik
**Ziel**: Professionelle Präsentation einer innovativen Vision

