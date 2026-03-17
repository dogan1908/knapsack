# Verdrängungsimpuls und Ersetzungswert: Eine relationale Matrixmethode für das 0/1-Knapsack-Problem

**Autor:** Dogan Balban — Independent Researcher  
**Datum:** März 2026  
**Sprache:** Deutsch  
**Status:** Preprint

---

## Zusammenfassung

Diese Arbeit stellt den *Matrix-Score* vor — eine neuartige relationale Heuristik für das 0/1-Knapsack-Problem. Die Methode basiert auf einer n×n-Proportionsmatrix, in der jede Ware gleichzeitig als Container und als Inhalt betrachtet wird.

Die zentrale Matrixzelle

$$M[i][j] = \left\lfloor \frac{w_i}{w_j} \right\rfloor \cdot \frac{v_j}{v_i}$$

misst den *Ersetzungswert*: wie viel wertvoller wäre der Gewichtsplatz von Ware *i*, wenn man ihn mit Exemplaren von Ware *j* füllt?

Der daraus abgeleitete Kern-Score

$$\bar{M}_j = \frac{1}{|\mathcal{C}_j|} \sum_{i \in \mathcal{C}_j} M[i][j]$$

ist **parameterfrei**, hat Komplexität **O(n²)** und ist **unabhängig von der Rucksackkapazität W**.

## Kernbeiträge

- **UKP-informierte 0/1-Heuristik:** Der Operator ⌊wᵢ/wⱼ⌋ stammt aus der Unbounded-Knapsack-Theorie (Simple Dominance), wird hier aber nicht zur Eliminierung, sondern zur relationalen Bewertung verwendet.
- **Parameterfreier Kern-Score:** M̄ⱼ enthält keine empirischen Koeffizienten — die Blockierungserkennung ist ein natürliches Nebenprodukt der Mittelwertbildung über die Container-Menge.
- **W-Unabhängigkeit:** Einziges nicht-triviales Bewertungsverfahren in der Knapsack-Literatur, das die Kapazität W nicht verwendet.
- **Konstruiertes Gegenbeispiel:** Der reine M̄ⱼ findet das DP-Optimum (134 €), wo Greedy v/w durch einen Blockierer scheitert (130 €).
- **Fourier-Analyse:** Frequenzspektrum-Vergleich von DP, Greedy und Matrix-Score zeigt die spektrale Energieverschiebung.

## Dateistruktur

```
├── knapsack_balban2026.tex      # LaTeX-Quellcode (Hauptdokument)
├── knapsack.bib             # Bibliographie (BibTeX)
├── knapsack_balban2026.pdf       # Kompiliertes Paper (25 Seiten)
├── README.md                # Diese Datei
└── LICENSE                  # CC BY 4.0
```

## Kompilierung

```bash
pdflatex knapsack_balban2026.tex
bibtex knapsack_balban2026
pdflatex knapsack_balban2026.tex
pdflatex knapsack_balban2026.tex
```

**Voraussetzungen:** TeX Live 2023+ oder MiKTeX mit folgenden Paketen:
`amsmath`, `amssymb`, `amsthm`, `tikz`, `pgfplots`, `booktabs`, `natbib`, `hyperref`, `mdframed`, `eurosym`, `algorithm`, `algpseudocode`

## Inhaltsverzeichnis des Papers

1. Einleitung und Motivation
2. Verwandte Arbeiten (Greedy, DP, Dominanz, UKP, QKP)
3. Formale Definition: Relationale Proportionsmatrix
   - Matrixzelle, Kern-Score M̄ⱼ, optionale Blockierungsstrafe
   - 7 formale Sätze mit Beweisen
   - UKP-Operator im 0/1-Kontext
4. Durchgerechnetes Beispiel: 7 Waren (mit Heatmap)
5. Algorithmus (Pseudocode + Flowchart)
6. Konstruiertes Gegenbeispiel: Blockierung durch die Skulptur
7. Empirischer Vergleich mit 8 Methoden über 5 Instanzklassen
8. Frequenzanalyse (DFT: DP vs. Greedy vs. Matrix-Score)
9. Laufzeitanalyse (v/w vs. K̄ⱼ vs. M̄ⱼ)
10. Sensitivität der optionalen Blockierungsstrafe
11. Diskussion (UKP-Einordnung, v/w als Spezialfall, Limitationen)
12. Fazit und Ausblick

## Zitation

```bibtex
@article{balban2026matrix,
  author  = {Balban, Dogan},
  title   = {Verdrängungsimpuls und Ersetzungswert: Eine relationale 
             Matrixmethode für das 0/1-Knapsack-Problem},
  year    = {2026},
  note    = {Preprint, Independent Research}
}
```

## Lizenz

Dieses Werk ist lizenziert unter [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

Sie dürfen das Material in jedwedem Format oder Medium vervielfältigen und weiterverbreiten, das Material remixen, verändern und darauf aufbauen — solange angemessene Urheber- und Rechteangaben gemacht werden.
