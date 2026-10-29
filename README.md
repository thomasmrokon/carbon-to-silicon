# CARBON TO SILICON

**Stegreif-Aufgabe · Bachelor Architektur · Hochschule Mainz · WS 2026/27**
Prof. Thomas Mrokon

*Vom gedanklichen Ursprung zum generativen Entwurfs-Konfigurator*

> 👉 **Neu bei GitHub oder beim Programmieren?** Starten Sie mit dem interaktiven
> Onboarding: **https://thomasmrokon.github.io/carbon-to-silicon/onboarding.html**
> (nach dem Anlegen Ihrer eigenen Kopie auch unter `…ihre-url…/onboarding.html`).

---

## Worum es geht

Agentische KI-Systeme verschieben die Rolle des Architekten: Nicht das manuelle
Zeichnen oder Programmieren steht im Zentrum, sondern die Fähigkeit, die **Systeme,
Regeln und Werkzeuge** zu definieren, die Entwürfe hervorbringen. Dieser Stegreif
erprobt diese Hypothese praktisch – als Brücke von kreativer Intelligenz auf
Kohlenstoff-Basis (Ihr Kopf als Ursprung) zu technischer Intelligenz auf
Silicium-Basis (die agentische Umsetzung).

Sie entwickeln **kein fertiges Gebäude, sondern ein funktionierendes generatives
Werkzeug**: einen Gebäude-Konfigurator, der aus einem **selbst definierten
Bauteil-Vokabular („Kit of Parts")** nach **Ihren Regeln** in Echtzeit ein drehbares
3D-Modell erzeugt. Die Geometrie wird aus dem Vokabular zusammengesetzt, nicht frei
modelliert.

## Der gemeinsame Kontext: eine Baulücke

Für alle gleich – das sichert Vergleichbarkeit und liefert den Widerstand, an dem
sich Ihr Regelsystem bewährt:

- Innerstädtische **Baulücke im Blockrand**, beidseitig an **Brandwände** grenzend.
- Straßenbreite **6–12 m**, Tiefe **bis 25 m**, Traufhöhe im Anschluss an den Bestand
  (**4–6 Vollgeschosse**).
- Belichtung nur von **Straßen- und Hofseite**.
- Die **Grundstücksbreite kann Eingabeparameter** Ihres Konfigurators sein.

Der Kontext ist im Scaffold (`index.html`) bereits als 3D-Geometrie hinterlegt und
**verbindlich**. Ihr Konfigurator baut *in dieses Volumen hinein*.

## Automatische Auswertung (DIN 277 & Kennwerte)

Der Scaffold misst **live** an Ihrer erzeugten Geometrie und zeigt ein Auswertungs-Panel:
**DIN 277 auf Massenebene** (BRI, BGF, Grundfläche), **Planungskennwerte** (Geschosse,
GRZ, GFZ – bezogen auf die Baulücke) sowie das **A/V-Verhältnis** und geschätzte
**CO₂-** und **Kosten**-Werte (BGF × didaktischer Platzhalterfaktor, im Code anpassbar).
So liefert Ihr Konfigurator auf Knopfdruck Daten zur ökologischen und ökonomischen
Vergleichbarkeit, die man sonst mühsam berechnen müsste. (Netto-Flächen nach DIN 277 –
NUF/VF/TF – sind auf Massenebene nicht ableitbar.)

## Ihr eigenes Bewertungskriterium

Über die feste Auswertung hinaus definieren Sie **mindestens ein eigenes, vergleichendes
Kriterium** und bauen es ein. Es muss **quantifizierbar** sein, **live auf Ihre Parameter
reagieren**, **im Tool angezeigt** werden und in der Reflexion **begründet** sein – *was ein
guter Entwurf ist, legen damit Sie fest.* Implementiert wird es in der markierten Funktion
`eigenesKriterium()` in `index.html`; das Ergebnis erscheint im Auswertungs-Panel.

*Zur Anregung (nicht verpflichtend):* Zirkularität/Rückbaubarkeit, Tageslichtangebot,
Anteil Flächen mit Außenbezug, Flexibilität/Umnutzbarkeit, Kosten je Nutzeinheit, graue Energie.

## Ablauf

| Phase | Zeit | Inhalt |
|---|---|---|
| Kick-off (Zoom) | Fr, 14:00 | Einführung, technische Voraussetzungen, Werkzeuge |
| **Offline-Phase (Kohlenstoff)** | Fr, ca. 14:30–18:00 | Kein Internet, keine Fachliteratur, keine KI – nur Kopf, Stift, Papier. Hier entsteht Ihr **Regelsystem**. Analoges Ergebnis bis 18:00 einreichen – **vor** jedem KI-Einsatz. |
| Entwicklung (Silicium) | Sa | Umsetzung mit KI-Agenten zum lauffähigen Konfigurator |
| Iteration | So | Testen, Bugfixing, README |
| **Abgabe** | Mo, bis 12:00 | **ZIP auf OLAT**: Offline-Artefakt, Repo-Link, Reflexion |
| Präsentation & Testrunde | Di, 12:00 (Zoom) | Kurzvorstellung, Test eines zugewiesenen Werkzeugs, strukturiertes Feedback |

## Abgaben

- **Offline-Artefakt** (Fr, bis 18:00): 1–3 handgezeichnete Blätter (A4/A3) als PDF.
  Pflicht ist ein **Regel-/Vokabularblatt** (Bausteine, Kombinationsregeln,
  Parameter), dazu Konzeptskizzen und/oder ein Ablaufdiagramm. Keine am Rechner
  erzeugten Inhalte.
- **Dieses Repository** (Mo): lauffähiger Konfigurator, über **GitHub Pages** im
  Browser erreichbar.
- **Reflexion** (Mo, max. 1 DIN-A4-Seite): siehe [`vorlagen/REFLEXION.md`](vorlagen/REFLEXION.md).
- **Peer-Feedback** (Di): siehe [`vorlagen/PEER-FEEDBACK.md`](vorlagen/PEER-FEEDBACK.md).

**Gesamtabgabe (Mo, bis 12:00):** als **eine ZIP-Datei auf OLAT** – das Offline-Artefakt
(PDF), eine Textdatei mit dem Link zu Ihrem Repository und die Reflexion gemeinsam.

## Bewertung (4 Kriterien, je 25 %)

Bewertet wird **nicht der (KI-geschriebene) Code**, sondern die architektonische
Haltung und die Nachvollziehbarkeit des Weges.

1. **Konzept & Regelsystem** – Tiefe und Originalität des Denkens in der Offline-Phase.
2. **Carbon-to-Silicon-Kohärenz** – nachvollziehbare Entwicklung vom Blatt zum Tool.
   Ein *begründeter* Kurswechsel zählt positiv, ein Bruch *ohne* Begründung negativ.
3. **Funktion & Gestaltung des Werkzeugs** – Zuverlässigkeit, Bedienbarkeit,
   gestalterische Qualität der erzeugten Entwürfe.
4. **Reflexion & Testrunde** – Qualität der Reflexion und des gegebenen Peer-Feedbacks.

---

## So starten Sie

1. **Oben rechts auf „Use this template" → „Create a new repository"** klicken und
   ein **öffentliches** Repository in Ihrem GitHub-Account anlegen.
2. Repository **klonen oder im Browser bearbeiten**. Für den Start genügt die
   `index.html`.
3. Lokal testen: `index.html` per **Doppelklick** im Browser öffnen.
4. **GitHub Pages aktivieren:** Repo → *Settings* → *Pages* → *Source:* „Deploy from a
   branch" → Branch **`main`**, Ordner **`/ (root)`** → *Save*. Nach ca. 1 Minute ist
   Ihr Tool unter `https://<ihr-name>.github.io/<repo>/` erreichbar.
5. Entwickeln Sie Ihren Konfigurator in der markierten Zone
   `=== HIER BEGINNT IHR KONFIGURATOR ===` in `index.html`.

## Arbeiten mit dem KI-Agenten

Übergeben Sie Ihrem Agenten die Datei
[`TECHNISCHE_ANFORDERUNGEN.md`](TECHNISCHE_ANFORDERUNGEN.md) als Rahmen und Ihr
Regel-/Vokabularblatt als Konzept. Tipp: Bildfähige Modelle können ein **Foto Ihres
handgezeichneten Regelblatts** einlesen – ein direkter Carbon→Silicon-Übergang.

## Ressourcen

- **KI-Agent** empfohlen (z. B. Claude Pro oder ChatGPT Plus), nicht verpflichtend.
- **Kostenlose Alternative – GWDG Academic Cloud:** <https://chat-ai.academiccloud.de/>
  (für die Programmierung v. a. *Qwen 3 Coder Next*, *GLM 5.3 Flash*, *DeepSeek V4 Flash*)
- **three.js-Dokumentation:** <https://threejs.org/docs/>
- **GitHub Pages – Einstieg:** <https://pages.github.com/>
