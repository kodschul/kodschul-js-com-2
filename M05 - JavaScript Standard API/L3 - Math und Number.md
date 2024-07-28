## JavaScript: Arbeiten mit Math und Number in JavaScript

JavaScript bietet eingebaute Objekte und Funktionen für mathematische Operationen und die Arbeit mit Zahlen. Im Folgenden sind einige grundlegende Konzepte und Codebeispiele zum Arbeiten mit Math und Number in JavaScript:

### Math-Objekt

Das `Math`-Objekt in JavaScript enthält eine Vielzahl von mathematischen Konstanten und Funktionen. Hier sind einige davon:

- `Math.PI`: Die Kreiszahl π.
- `Math.abs(x)`: Gibt den absoluten Wert von `x` zurück.
- `Math.round(x)`: Rundet `x` auf die nächste ganze Zahl.
- `Math.floor(x)`: Rundet `x` abwärts auf die nächstkleinere ganze Zahl.
- `Math.ceil(x)`: Rundet `x` aufwärts auf die nächstgrößere ganze Zahl.
- `Math.random()`: Gibt eine pseudozufällige Gleitkommazahl zwischen 0 und 1 zurück.

Beispiel:

```javascript
const radius = 5;
const area = Math.PI * Math.pow(radius, 2);
console.log('Fläche des Kreises:', area);
```

### Number-Objekt
Das Number-Objekt in JavaScript bietet nützliche Eigenschaften und Methoden zum Arbeiten mit Zahlen. Hier sind einige davon:

- Number.MAX_VALUE: Die größte darstellbare positive Zahl.
- Number.MIN_VALUE: Die kleinste darstellbare positive Zahl größer als 0.
- Number.isNaN(x): Überprüft, ob x NaN (Not a Number) ist.
- Number.isInteger(x): Überprüft, ob x eine ganze Zahl ist.
- Number.parseFloat(string): Parst eine Zeichenkette und gibt eine Gleitkommazahl zurück.
- Number.parseInt(string, radix): Parst eine Zeichenkette als Ganzzahl mit der angegebenen Basis (Radix) und gibt eine ganze Zahl zurück.

```javascript
const num1 = 10;
const num2 = 20;
console.log('Maximale Zahl:', Number.MAX_VALUE);
console.log('Summe:', num1 + num2);
```