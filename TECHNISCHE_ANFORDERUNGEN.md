# Technische Anforderungen

Der **empfohlene Standard** unten ist der schnellste, sichere Weg und entspricht dem
mitgelieferten Scaffold. **Ambitionierte Teams dürfen aufwändigere Stacks nutzen** – solange
die **Pflicht-Anforderungen** erfüllt bleiben. Den empfohlenen Block können Sie direkt an Ihren
KI-Agenten übergeben.

## Pflicht – unabhängig vom gewählten Stack
- **Öffentlich im Browser erreichbar** über eine URL, ohne lokale Installation für die
  Testenden (das hält die gemeinsame Präsentation einfach).
- **Keine Secrets/API-Keys im öffentlichen Code**, keine bezahlten KI-/Onlinedienst-Aufrufe zur
  Laufzeit. KI-Nutzung gehört in die Entwicklung, nicht in das laufende Tool.
- Der vorgegebene **Baulücken-/Blockrand-Kontext** wird eingehalten; Ihr Baukörper entsteht im
  vorgegebenen Volumen.
- **Parametrischer Konfigurator:** Eingaben erzeugen in Echtzeit ein 3D-Modell aus einem
  definierten **Kit of Parts** nach Ihren Regeln – nicht frei modelliert.
- Die **Kern-Auswertung** (DIN 277 auf Massenebene: BGF, BRI, Grundfläche; GRZ/GFZ) **und Ihr
  eigenes vergleichendes Kriterium** sind vorhanden und im Tool sichtbar.
- Das Ergebnis ist **als 3D exportierbar** (.obj oder .glTF).
- Öffentliches **GitHub-Repository** mit kurzer README (Konzept + Testanleitung + URL).

## Empfohlener Standard (Scaffold)
- Eine einzige, in sich geschlossene Web-Anwendung (`index.html`), rein clientseitig.
- Kein Backend, kein Server, keine Datenbank, kein Build-Schritt.
- 3D mit **three.js**, per CDN mit fixierter Version (z. B. `three@0.160.0`).
- Deployment über **GitHub Pages** (statisch, kostenlos, ein Klick).
- Läuft in aktuellem Chrome und Firefox, lädt ohne Konsolenfehler.

## Erlaubte Erweiterungen (für ambitionierte Teams)
- Build-Tools und Frameworks (z. B. Vite, React, Vue), WebGPU, parametrische/CAD-/IFC-
  Bibliotheken – alles erlaubt, solange die Pflicht-Anforderungen stehen.
- Ein **eigener Server/Backend** ist möglich, aber dann liegen Deployment *und* „läuft für
  alle" in Ihrer Verantwortung (GitHub Pages ist statisch). **Verlieren Sie nicht das
  Wochenende im Setup** – der Scaffold ist der sichere Weg, nicht die Obergrenze.

---

### Hinweis zum Scaffold
Die mitgelieferte `index.html` enthält bereits Szene, Kamera, Licht, OrbitControls, den
Baulücken-Kontext als geschlossenen **Blockrand mit Innenhof**, einen steuerbaren
**Sonnenstand** mit Sonnenbahn und Schlagschatten, die wichtigsten **Umgebungsmaße**,
Parameter-Slider, die **Export-Funktionen** und die feste **Auswertung** (DIN 277,
Planungskennwerte, A/V, CO₂/Kosten). Ihr Beitrag entsteht in den markierten Zonen
`=== HIER BEGINNT IHR KONFIGURATOR ===` (Kit of Parts + Regeln) und
`=== IHR EIGENES KRITERIUM ===`. Das UI dürfen Sie frei anpassen; weitere Darstellungen des
Modells sind ausdrücklich erwünscht.
