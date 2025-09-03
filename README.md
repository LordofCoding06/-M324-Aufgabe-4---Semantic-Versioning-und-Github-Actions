# M324 Aufgabe 4 – Semantic Versioning und GitHub Actions

## Vorarbeiten
Erstellt ein Repository in welchem ihr ein kleines VueJS Projekt erstellt:  
👉 [VueJS Quick Start](https://vuejs.org/guide/quick-start)

Wählt beim Erstellen des Projektes aus, dass für euch **Vitest**, **E2E Tests** und **ESLint** installiert/konfiguriert werden.  

Dies gibt euch Tasks, welche ihr in der Pipeline ausführen könnt.  

---

## Aufgaben

### Teil 1: Tags mit Semantic Versioning
- Erstellt einen **.git-hook**, welcher das Repository mittels Semantic Versioning taggt.  
- Dazu erstellt ihr ein Script (Sprache könnt ihr wählen), welches ihr dann im `.post-commit` Hook ausführt.  
- Das Script soll den jetzigen Tag prüfen und entsprechend der Commit Message einen neuen Tag erstellen nach den Regeln von **Semantic Versioning** und **Conventional Commits**.  

---

### Teil 2: Tags mittels GitHub Actions
- Nutzt das Script, welches ihr in Teil 1 erstellt habt, und wendet dieses als **GitHub Workflow** an.  

👉 [Beispiel-Workflow in der GitHub Doku](https://docs.github.com/de/actions/tutorials/create-an-example-workflow)

---

### Teil 3: Erst Tests & Build, dann Taggen
- Natürlich sollten Tags nur gemacht werden, wenn das Projekt auch einen Build macht.  
- Einen Build machen wir nur, wenn die Tests **grün** sind.  
- Erstellt zwei weitere Workflows, welche jeweils den **Build** und die **Unit Tests** laufen lassen (die Tasks findet ihr in der `package.json` des Projekts).  
- Der Tag-Workflow soll nur gestartet werden, wenn **Build** und **Test-Workflow** erfolgreich waren.  

👉 [Node.js Build & Test Tutorial in der GitHub Doku](https://docs.github.com/de/actions/tutorials/build-and-test-code/nodejs)
