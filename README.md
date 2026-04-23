# Marp Theme für die Mischok Academy

Dieses Repository enthält das offizielle Marp-Theme für Präsentationen der Mischok Academy sowie Beispiel-Präsentationen.

## 🚀 Schnellstart

### Voraussetzungen

Du benötigst die [Marp CLI](https://github.com/marp-team/marp-cli), um die Präsentationen zu rendern.

```bash
# Installation via npm
npm install -g @marp-team/marp-cli
```

### Präsentation als Server starten

Um eine Präsentation im Browser mit Live-Reload anzuzeigen:

```bash
marp --theme-set . -s examples
```
Die Präsentationen sind dann unter `http://localhost:8080` erreichbar.

### Als PDF exportieren

Um alle Präsentationen im `examples`-Ordner als PDF zu exportieren:

```bash
marp --theme-set . --pdf examples
```

## 🎨 Theme Details

Das Theme heißt `mischok-academy` und wird in der Markdown-Datei im YAML-Header aktiviert:

```yaml
---
marp: true
theme: mischok-academy
paginate: true
---
```

### Unterstützte Slide-Klassen

Du kannst verschiedene Layouts über Scoped Settings (`<!-- _class: name -->`) nutzen:

- `section`: Für Abschnittstrenner (Zentriert, großer Titel)
- `content`: Standard-Layout für Textinhalte
- `two-col`: Zwei-Spalten-Layout (nutzt `<div class="left">` und `<div class="right">`)
- `quote`: Für hervorgehobene Zitate
- `closing`: Abschlussfolie mit Kontaktinformationen

### Beispiel für ein Zwei-Spalten-Layout

```markdown
---
<!-- _class: two-col -->

# Überschrift

<div class="left">

- Punkt A
- Punkt B

</div>

<div class="right">

![Bildbeschreibung](bild.png)

</div>
```

## 📁 Projektstruktur

- `mischok-academy.css`: Die Definition des Marp-Themes.
- `examples/`: Beispiel-Präsentationen (z.B. ISO/OSI-Modell, Syntax-Highlighting).
- `README.md`: Diese Dokumentation.

## 🛠️ VS Code Integration

Für die beste Erfahrung in VS Code empfehlen wir die Erweiterung [Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode).

Um das lokale Theme in VS Code zu nutzen, füge dies zu deinen `.vscode/settings.json` hinzu:

```json
{
  "markdown.marp.themes": [
    "./mischok-academy.css"
  ]
}
```

## 💎 Nutzung in Obsidian

Du kannst dieses Theme auch in [Obsidian](https://obsidian.md/) verwenden, um Präsentationen direkt aus deinen Notizen zu erstellen:

1. Installiere das Community-Plugin **"Marp"** in Obsidian.
2. Kopiere die Datei `mischok-academy.css` in deinen Obsidian-Vault.
3. In den Einstellungen des Marp-Plugins unter "Themes" kannst du den Pfad zur CSS-Datei hinzufügen oder das Theme als Standard hinterlegen.
4. Stelle sicher, dass in deinem Markdown-Header `theme: mischok-academy` eingetragen ist.
