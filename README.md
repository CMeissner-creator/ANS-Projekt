# ANS-Projekt

Das ANS-Projekt hat zum Ziel einen 5,5 MHz Colpitts Oszilator zu entwerfen

- Kundenwünsche / Ursprüngliche Zielsetzung
- KiCad Projekte der Entwicklung
- Messwerte des Aufbau

Die Website wird automatisch aus dem Ordner `docs/` generiert.


# Kunden Anforderungen
- 5,5 MHz Mittenfrequenz (Zwischenfrequenz Fernseher)
- Eingang 0 V
- linear ± 0,5 V ≙ ± 0,5 MHz
- Bandbreite von 5 bis 6 MHz
- nicht lineare Verzerrung sehr klein
- Robuste Platine für anschaulichen Unterricht
- große Bauteile
- Spannungsteiler integriert
- Ein- und Ausgang BNC
- Ausgangswiderstand 50 Ω
- Frequenzdrift durch Gleichspannung korrigiert
- Kennlinienermittlung mit Gleichspannung
- Kurzschluss sicher

## Quellen für den Colpitts Oszillator
- [Elektroniktutor FM Modulation](https://www.elektroniktutor.de/signalkunde/fm.html)
- [Elektroniktutor Colpitts Oszillator](https://www.elektroniktutor.de/signalkunde/colpitts.html)

### Coilpitts Oszillator in Emitterschaltung für 125 kHz

Als erstes haben wir den Colpitts Oszillator für für 125 kHz von der Elektroniktutor
Seite in KiCad und danach auf einer Platine aufgebaut.

[Schaltplan als PDF](/assets/Colpitts_Oszillator.pdf)

Danach haben wir versucht diesen Oszilator auf 5,5 Mhz umzubauen:

[Schaltplan als PDF](/assets/Colpitts_Oszillator_5.5MHz.pdf)

In der NGSpice / KiCad Simulation funktioniert der Oszilator so, aber in der Realität nicht.
Das Problem ist, dass ein Colpitts Oszilator in der Emitterschaltung bei so hohen Frequenzen nicht funktioniert.
Die Millerkapazität, des Transistor, macht die Emitterschaltung unmöglich im MHz Bereich.

#### Colpitts Oszillator in Basisschaltung für 5,5 MHz

So sind wir schließlich bei einem Colpitts Oszillator in Basisschaltung gelandet.

[Schaltplan als PDF](/assets/FM-ELK.pdf)

Dieser funktioniert so im Steckbrettaufbau.
