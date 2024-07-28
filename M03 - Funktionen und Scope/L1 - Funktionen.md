## JavaScript: Funktionen in JavaScript: Definition und Verwendung

JavaScript-Funktionen ermöglichen es, Code zu organisieren, zu strukturieren und wiederzuverwenden. Sie spielen eine zentrale Rolle in der JavaScript-Programmierung. Im Folgenden sind einige grundlegende Konzepte und Codebeispiele zur Definition und Verwendung von Funktionen in JavaScript:

### Beispiel 1: Funktion ohne Parameter

```javascript
// Definition einer Funktion
function greet() {
  console.log('Hallo!');
}

// Aufruf der Funktion
greet();
```

In diesem Beispiel wird die Funktion greet definiert, die einfach "Hallo!" in die Konsole ausgibt. Die Funktion wird dann durch greet() aufgerufen.

### Beispiel 2: Funktion mit Parametern und Rückgabewert

```javascript
// Definition einer Funktion mit Parametern
function add(a, b) {
  return a + b;
}

// Aufruf der Funktion mit Argumenten
const sum = add(3, 5);
console.log(sum); // Ausgabe: 8
```

Hier wird die Funktion add definiert, die zwei Parameter a und b annimmt und deren Summe zurückgibt. Die Funktion wird mit den Argumenten 3 und 5 aufgerufen, und das Ergebnis wird in der Variablen sum gespeichert und anschließend ausgegeben.

### Beispiel 3: Funktion als Ausdruck

```javascript
// Funktion als Ausdruck
const multiply = function(a, b) {
  return a * b;
};

// Aufruf der Funktion
const result = multiply(4, 6);
console.log(result); // Ausgabe: 24
```

In diesem Beispiel wird die Funktion multiply als Funktionsausdruck definiert und anschließend aufgerufen. Funktionsausdrücke sind anonym und können einer Variablen zugewiesen werden.