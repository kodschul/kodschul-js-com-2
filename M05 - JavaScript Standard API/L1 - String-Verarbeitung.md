# JavaScript: String-Verarbeitung in JavaScript

JavaScript bietet eine Vielzahl von Funktionen und Methoden zur Verarbeitung von Zeichenketten (Strings). Von einfachen Operationen wie Zeichenkettenverkettung bis hin zu komplexeren Aufgaben wie Suchen und Ersetzen bietet JavaScript eine umfangreiche Unterstützung für die Arbeit mit Strings. Im Folgenden sind einige grundlegende Konzepte und Codebeispiele zur String-Verarbeitung in JavaScript:

## Beispiel 1: Zeichenkettenverkettung

```javascript
const str1 = 'Hallo';
const str2 = 'Welt';
const combinedStr = str1 + ', ' + str2 + '!';
console.log(combinedStr); // Ausgabe: Hallo, Welt!
```

In diesem Beispiel werden zwei Zeichenketten (str1 und str2) verkettet, um eine neue Zeichenkette (combinedStr) zu erstellen.

## Beispiel 2: Stringlänge

```javascript
const str = 'JavaScript';
const length = str.length;
console.log(length); // Ausgabe: 10
```

Hier wird die length-Eigenschaft verwendet, um die Länge einer Zeichenkette zu ermitteln.

## Beispiel 3: Zeichenkettenmanipulation

```javascript
const str = 'JavaScript ist großartig!';
const upperCaseStr = str.toUpperCase();
const lowerCaseStr = str.toLowerCase();
console.log(upperCaseStr); // Ausgabe: JAVASCRIPT IST GROßARTIG!
console.log(lowerCaseStr); // Ausgabe: javascript ist großartig!
```

In diesem Beispiel werden die Methoden toUpperCase() und toLowerCase() verwendet, um eine Zeichenkette in Groß- bzw. Kleinbuchstaben umzuwandeln.

## Beispiel 4: Zeichenkette suchen und ersetzen

```javascript
const str = 'JavaScript ist großartig!';
const replacedStr = str.replace('JavaScript', 'React');
console.log(replacedStr); // Ausgabe: React ist großartig!
```

Hier wird die replace()-Methode verwendet, um das erste Vorkommen einer Zeichenkette durch eine andere zu ersetzen.