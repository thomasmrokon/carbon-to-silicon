# Technische Anforderungen

Diese Rahmenbedingungen können Sie **direkt an Ihren KI-Agenten übergeben**.

## Zielprodukt
- Eine einzige, in sich geschlossene Web-Anwendung (`index.html`), die rein im Browser läuft.

## Architektur
- Kein Backend, kein Server, keine Datenbank, kein Build-Schritt – alles clientseitig.
- 3D mit **three.js**, eingebunden per CDN mit **fixierter Version** (hier: `three@0.160.0`).
- Keine Aufrufe an KI-/Onlinedienste zur Laufzeit. **Keine API-Keys im Code** (das Repo ist öffentlich).

## Lauffähigkeit
- Läuft in aktuellem **Chrome** und **Firefox** (Desktop).
- Öffnet per Doppelklick auf `index.html` **und** über eine GitHub-Pages-URL.
- Lädt **ohne Konsolenfehler** und zeigt ohne weitere Konfiguration sofort ein Ergebnis.

## Funktion
- Parametrischer Konfigurator: Eingaben erzeugen **in Echtzeit** ein drehbares 3D-Modell.
- Die Geometrie wird aus einem **definierten Bauteil-Vokabular (Kit of Parts)** nach
  **selbst definierten Regeln** zusammengesetzt – nicht frei modelliert.
- Der vorgegebene **Baulücken-Kontext** (Brandwände, Nachbarn, bebaubares Volumen) bleibt
  erhalten; Ihr Baukörper entsteht innerhalb dieses Volumens.
- **Export** des Ergebnisses als `.obj` oder `.glTF`.

## Abgabe / Repo
- Öffentliches GitHub-Repo mit `index.html`, ggf. Assets und `README`.
- `README`: drei Sätze Konzept + Testanleitung + Pages-URL.

---

### Hinweis zum Scaffold
Die mitgelieferte `index.html` enthält bereits Szene, Kamera, Licht, OrbitControls,
den Baulücken-Kontext, Parameter-Slider, die Export-Funktionen und eine **feste
Auswertung** (DIN 277 auf Massenebene, Planungskennwerte, A/V, CO₂/Kosten), die live an
Ihrer Geometrie misst. Ihr Beitrag entsteht ausschließlich in der markierten Zone
`=== HIER BEGINNT IHR KONFIGURATOR ===`; Kontext und Auswertung bleiben unverändert.
