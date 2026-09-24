# Finanzierungsentscheidung unter Steuer- und Inflationsunsicherheit

**Python-Fallstudie zu einer unternehmerischen Investitionsentscheidung | Business Analytics · Consulting · Data Science**

Ein Unternehmen plant eine Investition von 100.000. Soll es vorhandene Mittel einsetzen, einen Bankkredit aufnehmen oder zusätzliche Mittel der Eigentümer als Einlage beziehungsweise Darlehen nutzen? Dieses Projekt übersetzt die Frage in ein nachvollziehbares Entscheidungsmodell für die Jahre 2027–2032.

**[Analyse und Ergebnisse im Jupyter Notebook öffnen](./finanzierungsanalyse.ipynb)**

## Ergebnis auf einen Blick

Für die modellierte Personengesellschaft und einen festgelegten Eigentümerhaushalt erzielt **F1 – Finanzierung aus vorhandenen Unternehmensmitteln – unter den Referenzannahmen das höchste Endvermögen**.

| Zusätzlich 100.000 privat verfügbar? | Vergleichbare Finanzierungen | Beste Option im Modell | Endvermögen 2032 |
|---|---|---|---:|
| Nein | Eigene Mittel oder Bankkredit | Eigene Mittel (F1) | 155.555,83 |
| Ja | Eigene Mittel, Einlage, Gesellschafterdarlehen oder Bankkredit | Eigene Mittel (F1) | 312.513,37 |

Im Ja-Fall beträgt der berechnete Vorsprung von F1 gegenüber dem Bankkredit **7.767,35**. Die beiden Tabellenzeilen haben unterschiedliche Anfangsausstattungen und werden deshalb nicht gegeneinander bewertet.

**Die Empfehlung ist bedingt:** Das Modell verwendet unter anderem 12 % Kreditzins und 10 % Guthabenzins aus einem historischen Lehrbuchbeispiel. Das sind keine aktuellen Marktangebote. Ob F1 praktisch sinnvoll ist, hängt auch davon ab, welche Liquiditätsreserve das Unternehmen für sein laufendes Geschäft benötigt.

## Beratungsfrage und Vorgehen

Der erste Schritt ist eine Frage, die den Vergleich verändert: **Verfügen die Eigentümer zusätzlich zu den 100.000 im Unternehmen über weitere 100.000 privat?** Nur Finanzierungen mit derselben anfänglichen Mittelausstattung werden innerhalb eines Falls verglichen.

Das Notebook führt anschließend durch vier Analyseschritte:

1. **Finanzierbarkeit und Zahlungsströme:** Eigene Mittel (F1), zusätzliche Einlage (F2), Gesellschafterdarlehen (F4) und externer Kredit (F5) werden über sechs Jahre abgebildet.
2. **Steuern und Eigentümerperspektive:** Vereinfachte Körperschaft-, Gewerbe-, Einkommen- und Kapitalertragsteuerrechnungen werden dort ergänzt, wo die jeweiligen Voraussetzungen im Fallmodell festgelegt sind.
3. **Szenarien und Kaufkraft:** Veröffentlichte Inflationswerte für 2027 und 2028 sowie ausdrücklich eigene Annahmen für 2029–2032 zeigen, wie sich nominale Endbeträge in Preisen von 2026 einordnen lassen.
4. **Sensitivität und Entscheidung:** Das Modell prüft alternative spätere Kreditzinsen, Gesellschafterzinsen und Grenzen der Kreditrückzahlung. Ergebnisse werden als bedingte Entscheidung interpretiert.

## Was das Projekt zeigt

- **Business Analytics:** Eine offene Managementfrage wird in vergleichbare Fälle, Zahlungsströme und Entscheidungsgrößen übersetzt.
- **Consulting:** Die Empfehlung nennt ihre Voraussetzungen und trennt verfügbare Mittel, Endvermögen und betriebliche Liquidität.
- **Data Science:** Das Notebook dokumentiert Eingaben, implementiert Szenario- und Sensitivitätsrechnungen in Python und prüft ausgewählte Ergebnisse auf rechnerische Konsistenz. Es trainiert kein Prognose- oder Machine-Learning-Modell.

**Werkzeuge:** Python, pandas, Matplotlib und Jupyter Notebook.

## Daten und Modellgrenzen

Die Investitions- und Zinswerte orientieren sich am historischen Lehrbuchbeispiel von König und Wosnitza, *Betriebswirtschaftliche Steuerplanungs- und Steuerwirkungslehre* (2004). Für die Inflation 2027 und 2028 nutzt das Modell die [Deutschland-Prognose der Deutschen Bundesbank vom 12. Juni 2026](https://www.bundesbank.de/de/presse/pressemitteilungen/deutschland-prognose-der-bundesbank-energiepreis-schock-bremst-konjunkturerholung-964728). Werte für 2029–2032 sind gekennzeichnete Szenarioannahmen. Steuerliche Regeln und Vereinfachungen sind im Notebook mit Quellen und Rechtsstand dokumentiert.

Die Resultate sind **keine Vorhersage und keine individuelle Steuer- oder Finanzierungsberatung**. Es werden weder Eintrittswahrscheinlichkeiten geschätzt noch Zufallsvariablen simuliert. Die Liquiditätsprüfung betrachtet modellierte Jahreszeitpunkte, keine täglichen Zahlungsbedarfe.

Für die Kapitalgesellschaft werden einzelne Ergebnisse auf Unternehmens- und Eigentümerebene gezeigt. Insbesondere liegen für Einlage und Gesellschafterdarlehen keine vollständig vergleichbaren Nettoauszahlungen an die Eigentümer vor. **Das Projekt leitet deshalb keine Rangfolge der Rechtsformen ab.**

## Mögliche Erweiterungen

Ein separates Zeitreihenprojekt könnte Inflations- oder Zinsprognosen erstellen und anhand ihrer Prognosegüte beurteilen. Ein eigenes Bonitätsmodell würde geeignete Unternehmens- und Ausfalldaten erfordern.
