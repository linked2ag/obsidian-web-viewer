# Obsidian Web Viewer
Ein hoch-interaktiver, leichtgewichtiger und vollständig lokaler Web-Client für deine Obsidian-Tresore (Vaults). Diese Anwendung besteht aus einer einzigen, autarken HTML-Datei und ermöglicht es dir, deine Markdown-Notizen direkt im Browser zu lesen, live zu editieren und die Beziehungen deiner Gedanken visuell zu analysieren.

# Key Features
## Lokaler Dateizugriff (Direct Read & Write)
- Kein Server benötigt: 100 % Client-seitig im Browser. Deine Daten bleiben absolut privat und verlassen niemals deinen Computer.
- Dateisystem-Anbindung: Über die moderne File System Access API (unterstützt von Chrome, Edge, Opera) liest die App deine Notizen nicht nur ein, sondern schreibt Änderungen beim Speichern direkt zurück auf deine Festplatte.
- Stille Synchronisation: Mit dem Refresh-Button lässt sich der Tresor im Hintergrund aktualisieren, um Änderungen von außerhalb sofort zu übernehmen.
## Authentisches Obsidian-UI & UX
- Originalgetreues Light-Theme: Basierend auf den visuellen Vorgaben von Obsidian, inklusive originalem, geometrisch perfektem Oktaeder-Logo.
- Strukturierte Ordner-Navigation: Übersichtlicher, fett formatierter Dateibaum mit grauer Hintergrundschattierung und gelben Ordner-Icons. Lange Seitennamen werden automatisch umgebrochen und nicht abgeschnitten.
- Workspace-Tabs mit Kontextmenü: Navigiere flüssig über Tabs. Mit einem Rechtsklick (Context Menu) kannst du einzelne Tabs schließen oder alle anderen Tabs im Workspace mit einem Klick aufräumen.
- Responsive Sidebar: Der Bereich für "Local Relations" (Eingehende Backlinks und ausgehende Verweise) lässt sich mit einem Klick vollständig ein- und ausklappen.
## High-Fidelity D3.js Graph View
- Optimierter D3-Simulations-Algorithmus: Ausgelegt für maximale Übersichtlichkeit und Lesbarkeit. Nodes stoßen sich stark genug ab, um auch lange Seitennamen gut darzustellen (Zeilenumbruch ab 30 Zeichen).
- Interaktive Fokussierung:
- Beim Hovern über einen Knoten oder eine Beschriftung werden alle anderen Beschriftungen sanft abgedunkelt (Opacity 0.15), um den Pfad visuell hervorzuheben.
- Beim Klick auf einen Node (Dot) wird dieser farblich markiert und nur die Beschriftungen der direkt verknüpften Nachbarn werden vollständig schwarz dargestellt.
- Filter-Modal für Verzeichnisse: Schließe Ordner wie das Root-Verzeichnis (mit Systemdateien wie claude.md oder index.md) standardmäßig aus und blende sie nur bei Bedarf über das integrierte Filter-Modal ein.
## Broken Link Scanner & Kapitel-Verknüpfung
- Zweistufige Reparatur: Wähle beim Korrigieren unaufgelöster Querverweise im ersten Schritt die Zielseite und im zweiten Schritt (optional) ein spezifisches Kapitel (Überschrift) aus.
- Shift-Click Shortcut: Halte die Shift-Taste gedrückt und klicke auf einen beliebigen WikiLink in der Notiz-Vorschau, um sofort das Verknüpfungs-Fenster zu öffnen und den Link umzurouten.
- Intelligente Ignorierung: Interne System-Dateien (wie claude.md) werden bei der automatischen Analyse auf kaputte Links ignoriert.
# Technologie-Stack
- Frontend Framework: Vanilla JS / HTML5 / CSS3
- Styling: Tailwind CSS (Utility-First Design)
- Icons: Lucide Icons (Native Obsidian-Ästhetik)
- Markdown Parser: Marked.js
- Daten-Visualisierung: D3.js (Force-Directed Graph Simulation)
# Installation & Schnellstart
Da das Projekt als Single-File-App konzipiert ist, ist die Einrichtung in Sekunden erledigt:
1. Datei herunterladen: Lade dir die Datei obsidian_viewer.html herunter.
2. Im Browser öffnen: Doppelklicke auf die Datei, um sie in deinem Standard-Browser zu öffnen.
3. Vault laden: Klicke im Startbildschirm auf Select Vault Folder und wähle den Stammordner deines Obsidian-Tresors aus.
4. Berechtigung erteilen: Bestätige die Browser-Abfrage für Lese- und Schreibrechte (erforderlich, wenn du Notizen direkt aus der Web-App editieren und speichern möchtest).
# Bedienungshinweise
## Navigation
- Einfacher Klick: Öffnet die ausgewählte Notiz im aktuell aktiven Tab.
- Ctrl / Cmd + Klick: Öffnet die ausgewählte Notiz oder den Graph-Knoten in einem neuen, separaten Tab.
- Scroll-to-Top: Beim Klicken auf eine Seite oder einen Link wird der Editor-Bereich automatisch wieder an den Seitenanfang gescrollt (außer bei direktem Sprung zu einer Kapitel-Überschrift).
## Suchen & Hervorheben
- Nutze die Suchfunktion in der Seitenleiste. Wenn du eine Notiz aus den Suchergebnissen öffnest, werden alle Vorkommen deines Suchbegriffs direkt im Text markiert.
- Wortgrenzen-Schutz: Die Suche trennt keine Wörter auf (eine Suche nach "buch" markiert den Teil in "Notizbuch", ohne das Wort in "Notiz buch" zu spalten).
- Sobald du zurück in die Dateiansicht ("Files") wechselst, werden alle Such-Markierungen automatisch entfernt.
# Privatsphäre & Sicherheit
Diese Anwendung erhebt keine Daten, setzt keine Cookies und baut keine Verbindung zu externen Datenbanken auf. Alle eingelesenen Dateien deines Obsidian-Tresors werden ausschließlich lokal im Arbeitsspeicher deines Webbrowsers verarbeitet. Das Speichern erfolgt direkt über die Sandbox-Schnittstelle deines Betriebssystems.
# Lizenz
Dieses Projekt ist unter der MIT-Lizenz lizenziert. Siehe die LICENSE-Datei für Details.
