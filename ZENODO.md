# Zenodo Upload — Metadaten

## Titel
Verdrängungsimpuls und Ersetzungswert: Eine relationale Matrixmethode für das 0/1-Knapsack-Problem

## Autoren
Balban, Dogan (Independent Researcher)

## Publikationsdatum
2026-03-18

## Typ
Preprint

## Sprache
Deutsch (deu)

## Lizenz
Creative Commons Attribution 4.0 International (CC-BY-4.0)

---

## Beschreibung (für Zenodo-Feld "Description")

Diese Arbeit stellt den Matrix-Score vor — eine neuartige relationale Heuristik für das 0/1-Knapsack-Problem. Im Gegensatz zu klassischen Greedy-Verfahren, die jede Ware isoliert durch ihren Effizienzquotienten v/w bewerten, betrachtet der Matrix-Score jede Ware gleichzeitig als Container und als Inhalt: die Matrixzelle M[i][j] = ⌊wᵢ/wⱼ⌋ · vⱼ/vᵢ quantifiziert den Ersetzungswert — wie viel wertvoller der Gewichtsplatz von Ware i wäre, wenn man ihn mit Ware j füllt.

Während klassische Greedy-Verfahren eine eindimensionale Größe (Effizienz v/w) optimieren, sucht der Matrix-Score den Gleichgewichtspunkt zwischen dem Nutzwert einer Ware und ihrem strukturellen Verdrängungsimpuls innerhalb des Warenkollektivs.

Der zentrale Operator ⌊wᵢ/wⱼ⌋ stammt aus der Unbounded-Knapsack-Theorie (Simple Dominance nach Kellerer et al., 2004; Threshold-Dominanz nach Andonov et al., 2000). Die vorliegende Arbeit verwendet ihn erstmals nicht zur Eliminierung dominierter Items, sondern als Baustein einer relationalen Bewertung im 0/1-Kontext — eine Brücke zwischen UKP- und 0/1-KP-Theorie, die in der Literatur nicht vorhanden ist.

Der daraus abgeleitete Kern-Score M̄ⱼ (mittlerer Ersetzungswert über alle aufnehmenden Container) ist parameterfrei, hat Komplexität O(n²) und ist unabhängig von der Rucksackkapazität W.

Die Arbeit umfasst:
• Vollständige formale Herleitung mit 7 bewiesenen Sätzen
• Durchgerechnetes 7-Waren-Beispiel mit farbkodierter Heatmap
• Konstruiertes Gegenbeispiel, in dem der parameterfreie M̄ⱼ das DP-Optimum findet, wo Greedy v/w versagt
• Empirischer Vergleich mit 8 publizierten Methoden über 5 Instanzklassen
• Fourier-Analyse der Frequenzsignaturen verschiedener Auswahlmethoden
• Laufzeitanalyse: reine Ganzzahl-Variante K̄ⱼ vs. Ersetzungswert M̄ⱼ
• Sensitivitätsanalyse der optionalen Blockierungsstrafe

---

## Keywords (für Zenodo-Feld "Keywords")

knapsack problem
0/1 knapsack
combinatorial optimization
heuristic
greedy algorithm
relational matrix
replacement value
displacement impulse
proportional matrix
UKP operator
simple dominance
threshold dominance
unbounded knapsack
W-independent heuristic
blocking detection
item packing
integer programming
NP-hard
Fourier analysis
spectral energy
parameterfree score
operations research

---

## Verwandte Identifikatoren (Related Identifiers)

Kellerer, H., Pferschy, U., & Pisinger, D. (2004). Knapsack Problems. Springer.
  ISBN: 978-3-540-40286-2

Andonov, R., Poirriez, V., & Rajopadhye, S. (2000). Unbounded knapsack problem: Dynamic programming revisited.
  DOI: 10.1016/S0377-2217(99)00265-9

Dantzig, G. B. (1957). Discrete-variable extremum problems.
  DOI: 10.1287/opre.5.2.266

---

## Empfohlene Zenodo-Communities

- Operations Research
- Combinatorial Optimization
- Mathematical Programming
- Computer Science — Algorithms

---

## .zenodo.json (optional, für automatische Metadaten bei GitHub-Integration)

```json
{
  "title": "Verdrängungsimpuls und Ersetzungswert: Eine relationale Matrixmethode für das 0/1-Knapsack-Problem",
  "upload_type": "publication",
  "publication_type": "preprint",
  "description": "A novel relational heuristic for the 0/1 knapsack problem based on an n×n proportional matrix. Each item is simultaneously treated as container and content. The core score M̄ⱼ is parameter-free, O(n²), and independent of knapsack capacity W. Uses the UKP dominance operator ⌊wᵢ/wⱼ⌋ not for elimination but for relational scoring — a bridge between unbounded and 0/1 knapsack theory.",
  "creators": [
    {
      "name": "Balban, Dogan",
      "affiliation": "Independent Researcher"
    }
  ],
  "keywords": [
    "knapsack problem",
    "0/1 knapsack",
    "combinatorial optimization",
    "heuristic",
    "relational matrix",
    "replacement value",
    "displacement impulse",
    "UKP operator",
    "simple dominance",
    "W-independent",
    "parameter-free",
    "operations research"
  ],
  "license": "CC-BY-4.0",
  "language": "deu",
  "access_right": "open"
}
```
