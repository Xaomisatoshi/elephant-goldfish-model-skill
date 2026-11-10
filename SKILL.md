---
name: elephant-goldfish-model
description: Führt einen strukturierten, spezifikationsgetriebenen Entwicklungsprozess nach dem Elephant-Goldfish-Modell (EGM) durch. Nutze diesen Skill, wenn der Nutzer das Elephant-Goldfish-Modell, EGM, Spec-Driven Development erwähnt, Software-Features gründlich vor dem Coden planen möchte oder einen unvoreingenommenen Review (Goldfish Review) eines Entwurfs benötigt.
---

# Elephant-Goldfish-Modell

Ein strukturierter Workflow für die Software- und Feature-Entwicklung, der Denken und Coden trennt. Er nutzt den vollen Projektkontext zur Konzeption (Elefant) und wechselt anschliessend in eine isolierte, unvoreingenommene Perspektive (Goldfisch), um Schwachstellen und Annahmen aufzudecken, bevor Code entsteht.

## Wann dieser Skill genutzt wird

- Der Nutzer möchte eine Software, ein Feature oder ein Skript entwickeln und vorab sauber spezifizieren.
- Der Nutzer erwähnt explizit "Elephant-Goldfish", "EGM" oder "Spec-Driven Development".
- Ein vorhandener Architekturentwurf oder ein Konzept soll schonungslos auf Logiklücken, Sicherheitsrisiken und blinde Flecken geprüft werden.

## Schritte des Workflows

### 1. Elefanten-Phase: Brainstorming und Konzept

In dieser Phase nutzt der Agent den gesamten Kontext, um die Vision des Nutzers zu erfassen.

- Kläre Ziel, Problemstellung und Nicht-Ziele (Out of Scope).
- Stelle 2 bis 3 gezielte Fragen zu Randbedingungen, Datenflüssen und Annahmen.
- Erstelle ein kompaktes Konzept (Concept Brief) in Markdown.
- Wichtig: In dieser Phase wird noch keine einzige Zeile Implementierungscode geschrieben.

### 2. Spezifikations-Entwurf (Design Spec)

Giesse das Konzept in ein klares, technisches Entwurfsdokument mit folgenden Abschnitten:

- Ziel und Motivation
- Systemgrenzen und Nicht-Ziele
- Architektur und Datenfluss
- Schnittstellen und Datenmodelle
- Fehlerbehandlung und Edge Cases

### 3. Goldfisch-Review (Unvoreingenommene Prüfung)

Schlüpfe in die Rolle des "Goldfischs" (Reviewer ohne Gedächtnis der Vordiskussion):

- Betrachte ausschliesslich das vorliegende Spezifikationsdokument.
- Prüfe, ob das Dokument ohne Vorwissen vollständig verständlich und umsetzbar ist.
- Identifiziere unklare Formulierungen, implizite Annahmen, Sicherheitslücken und fehlende Edge Cases.
- Gib konkretes Feedback gegliedert nach Schweregrad (Blocker, Empfehlungen, Detailfragen).

### 4. Bereinigung und Freigabe

- Arbeite das Feedback des Goldfischs in die Spezifikation ein.
- Präsentiere die bereinigte Spezifikation dem Nutzer zur Freigabe.
- Beginne erst mit der Implementierung, wenn der Nutzer den Entwurf explizit absegnet.

## Wichtige Regeln (Gotchas)

- Niemals vorzeitig Code generieren. Der gesamte Mehrwert von EGM liegt im vorherigen Durchdenken.
- Der Goldfisch darf kein implizites Vorwissen aus dem Chatverlauf voraussetzen. Wenn ein Detail im Entwurfsdokument fehlt, muss der Goldfisch es als Lücke bemängeln.
- Trenne Entwurfs- und Review-Phasen visuell und inhaltlich klar voneinander.
- Halte die Dokumentation präzise und frei von überflüssigen Fülltexten.
