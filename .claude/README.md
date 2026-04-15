# `.claude/` — Claude-Code-Konfiguration dieses Repos

Alles hier ist eingecheckt und versioniert; jede Claude-Code-Session liest
die Inhalte automatisch.

## Inhalt

```
.claude/
├── agents/             projekt-spezifische Subagenten
│   ├── solver.md        unabhängige Lösung einer HÜ
│   ├── scribe.md        handschrift-transkription
│   └── reviewer.md      doppel-check zweier lösungen
│
└── commands/           eigene slash-commands
    └── hu-review.md     orchestriert solver + scribe + reviewer
```

## Philosophie

Siehe `../lernplan/doppelcheck-workflow.md`.
Siehe `../CLAUDE.md` — Abschnitt "A. Lösungs-Review".

## Wenn ein Agent schlechte Outputs produziert

Iterativ verbessern: Datei in `.claude/agents/<name>.md` bearbeiten,
neuen Durchlauf starten. Die Agent-Prompts sind bewusst defensiv
geschrieben ("NICHT rechnen", "NICHT lesen", ...), weil sie sonst
auseinanderdriften. Regeln nicht aufweichen ohne Grund.
