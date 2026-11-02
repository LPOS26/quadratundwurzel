# Quadratzahlen und Wurzeln üben

Ein kleines Übungsspiel für den Mathematikunterricht. Schüler:innen trainieren die Quadratzahlen von 1 bis 25, die Wurzeln dieser Quadratzahlen als Gegenoperation und Rechenaufgaben, die sich mit Wurzelgesetzen im Kopf lösen lassen.

Das Spiel besteht aus **einer einzigen HTML-Datei**. Es braucht keine Installation, keine Bibliotheken und keine Internetverbindung.

## Schnellstart

1. Die Datei `quadratzahlen-spiel.html` herunterladen.
2. Per Doppelklick im Browser öffnen. Das funktioniert am Computer, Tablet und Smartphone.
3. Aufgabenart wählen und auf **Runde starten** klicken.

Die Datei lässt sich auch per E-Mail, USB-Stick oder Schulplattform an Schüler:innen verteilen.

## Aufgabenarten

| Modus | Beispiel | Beschreibung |
| --- | --- | --- |
| Quadrieren | 7² = ? | Quadratzahlen berechnen |
| Wurzel ziehen | √49 = ? | Gegenoperation: die Wurzel einer Quadratzahl bestimmen |
| Gemischt | 7² = ? und √49 = ? | Beide Aufgabentypen in zufälliger Reihenfolge |
| Rechentricks, leicht | √3 · √75 = ? oder √75 : √3 = ? | Eine Wurzel so zerlegen, dass √3 · √3 = 3 genutzt werden kann |
| Rechentricks, mittel | √8 · √18 = ? | Beide Wurzeln zerlegen und die Faktoren zusammenfassen |

Bei den Rechentricks ist das Ergebnis immer eine ganze Zahl (höchstens 100), damit die Aufgaben im Kopf lösbar bleiben.

**Beispiel für einen Rechenweg (leicht):**

```text
√3 · √75 = √3 · √3 · √25 = 3 · 5 = 15
```

## Einstellungen

- **Zahlenbereich:** 1 bis 10, 15, 20 oder 25 (für Quadrieren, Wurzel ziehen und Gemischt)
- **Anzahl der Aufgaben:** 10, 20 oder 30 pro Runde
- **Schwierigkeit:** leicht oder mittel (nur bei Rechentricks)

## Funktionen

- Jede Zahl kommt dran, bevor sich Zahlen wiederholen.
- Richtige Antworten gehen automatisch weiter, bei Fehlern wird die Lösung erklärt.
  - Bei Quadratzahlen und Wurzeln zeigt ein Quadrat auf Karopapier, dass die Seitenlänge und die Fläche zusammengehören.
  - Bei den Rechentricks wird der vollständige Rechenweg angezeigt.
- Auswertung am Ende der Runde mit Punkten, Zeit und längster Serie.
- Die Fehler werden aufgelistet und können mit **Fehler üben** gezielt wiederholt werden.
- Der Bestwert wird pro Einstellung im Browser gespeichert (`localStorage`).
- Tabelle der Quadratzahlen zum Nachschauen auf der Startseite.
- Bedienung per Tastatur: Antwort eingeben, mit `Enter` prüfen und mit `Enter` weiter.
- Helles und dunkles Farbschema, passend zur Geräteeinstellung.

## Auf GitHub Pages veröffentlichen

Wenn das Spiel direkt im Browser unter einer eigenen Adresse laufen soll:

1. Die Datei im Repository in `index.html` umbenennen (oder eine `index.html` anlegen, die darauf verweist).
2. Im Repository unter **Settings → Pages** den Branch (z. B. `main`) und den Ordner `/ (root)` auswählen.
3. Nach kurzer Zeit ist das Spiel unter `https://<benutzername>.github.io/<repository>/` erreichbar.

## Anpassen

Alle Einstellungen und der Aufgabengenerator stehen im `<script>`-Bereich am Ende der Datei.

- **Rechentricks:** Die Funktion `makeTrick()` erzeugt die Aufgaben. Die verwendeten Grundzahlen stehen in der Liste `primes`, die Faktoren in den `pick([...])`-Aufrufen. Der Wert `ans > 100` begrenzt die Größe der Ergebnisse.
- **Farben:** Die Farben sind als CSS-Variablen in `:root` definiert, getrennt für helles und dunkles Schema.
- **Texte:** Alle Texte sind auf Deutsch und direkt im HTML bzw. in der Auswertung (`finish()`) zu finden.

## Technische Hinweise

- Reines HTML, CSS und JavaScript, keine externen Abhängigkeiten
- Funktioniert in aktuellen Versionen von Chrome, Edge, Firefox und Safari
- Es werden keine Daten an einen Server gesendet. Gespeichert werden nur die Bestwerte lokal im Browser.

## Lizenz

Hier die gewählte Lizenz eintragen, zum Beispiel MIT, und eine passende `LICENSE`-Datei im Repository ablegen.
