# JavaScript: Umgang mit Datum und Zeit

Die Arbeit mit Datum und Zeit in JavaScript ist von zentraler Bedeutung für viele Anwendungen, sei es für die Darstellung von Kalendern, das Berechnen von Zeitspannen oder das Planen von Aufgaben. Im Folgenden sind einige grundlegende Konzepte und Codebeispiele zum Umgang mit Datum und Zeit in JavaScript:

## Beispiel 1: Erstellen eines Datumsobjekts

```javascript
// Aktuelles Datum und Uhrzeit
const currentDate = new Date();
console.log(currentDate);

// Ein spezifisches Datum und Uhrzeit erstellen (Jahr, Monat (0-11), Tag, Stunde, Minute, Sekunde, Millisekunde)
const specificDate = new Date(2024, 3, 14, 10, 30, 0, 0);
console.log(specificDate);
```

In diesem Beispiel werden ein aktuelles Datum und eine spezifische Datum/Uhrzeit-Kombination erstellt.

## Beispiel 2: Formatieren von Datum und Uhrzeit

```javascript
// Formatieren eines Datums als String (z.B. "14.04.2024")
const formattedDate = currentDate.toLocaleDateString('de-DE');
console.log(formattedDate);

// Formatieren einer Uhrzeit als String (z.B. "10:30:00")
const formattedTime = currentDate.toLocaleTimeString('de-DE');
console.log(formattedTime);

// Formatieren von Datum und Uhrzeit als String (z.B. "14.04.2024, 10:30:00")
const formattedDateTime = currentDate.toLocaleString('de-DE');
console.log(formattedDateTime);
```

Hier werden verschiedene Methoden zur Formatierung von Datum und Uhrzeit als String mithilfe der toLocaleDateString(), toLocaleTimeString() und toLocaleString() Funktionen gezeigt.

## Beispiel 3: Berechnen von Zeitspannen

```javascript
// Berechnen der Differenz zwischen zwei Datumsobjekten in Millisekunden
const diffInMilliseconds = specificDate - currentDate;
console.log(`Differenz in Millisekunden: ${diffInMilliseconds}`);

// Berechnen der Differenz in Tagen
const diffInDays = diffInMilliseconds / (1000 * 60 * 60 * 24);
console.log(`Differenz in Tagen: ${diffInDays}`);
```

Dieses Beispiel zeigt, wie man die Differenz zwischen zwei Datumsobjekten berechnet, sowohl in Millisekunden als auch in Tagen.