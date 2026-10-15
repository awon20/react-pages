# React auf GitHub Pages

Kleine React-Demo zum Veröffentlichen einer Single Page Application mit GitHub Pages und GitHub Actions.

## Umfang

- React-Beispielseite
- Getrennter Quellcode- und Veröffentlichungsbranch
- Vorhandener GitHub-Actions-Workflow für das Deployment

## Wartungsstand

Die Sicherheits- und Abhängigkeitsänderungen werden in [PR #1](https://github.com/awon20/react-pages/pull/1) verfolgt. Sie sind noch nicht in den Quellcode-Hauptbranch übernommen. Die README-Ergänzung führt diesen Pull Request nicht zusammen.

## Branches

- `gh-pages`: Standardbranch mit erzeugten Website-Dateien und dieser Übersicht.
- [`master`](https://github.com/awon20/react-pages/tree/master): React-Quellcode, Paketdateien und Entwicklungsgrundlage.

Änderungen am Programm im Quellcode-Branch vornehmen. Bei einer erneuten Veröffentlichung sollte diese README im Veröffentlichungsbranch erhalten bleiben.

## Lokal starten

Die folgenden Befehle verwenden ausdrücklich den vorbereiteten Wartungsbranch. Dessen Änderungen sind noch in Prüfung; offene Paketwarnungen stehen im zugehörigen PR. Der bisherige Hauptbranch verwendet teilweise ältere Build-Werkzeuge und kann mit neueren Node-Versionen fehlschlagen.

Voraussetzungen: Git, Node.js und npm. Die lokalen Web-Builds des Wartungsstands wurden mit Node.js 24.19.0 und npm 11.21.0 geprüft. Ein erfolgreicher Build bedeutet keine vollständige Behebung aller Paketwarnungen.

```sh
git clone --branch codex/security-maintenance-2026-10-13 https://github.com/awon20/react-pages.git
cd react-pages
npm ci --ignore-scripts
npm start
```

Die vom Entwicklungsserver ausgegebene lokale Adresse öffnen. Zum Beenden im Terminal `Ctrl+C` drücken.

## Build und Prüfungen

```sh
npm run build
npm audit
```

Der statische Web-Build liegt in `build/`. `npm test` startet den konfigurierten Test-Runner; die Existenz des Skripts allein belegt keine vollständige Testabdeckung.

## Projektstruktur

- [`src/App.js`](https://github.com/awon20/react-pages/blob/master/src/App.js)
- [`public`](https://github.com/awon20/react-pages/tree/master/public)
- [`.github/workflows`](https://github.com/awon20/react-pages/tree/master/.github/workflows)

## Beiträge

Änderungen mit einer kurzen Beschreibung und passenden Prüfergebnissen als Pull Request einreichen. Keine Zugangsdaten, privaten Schlüssel oder lokalen Abhängigkeitsordner hinzufügen.
