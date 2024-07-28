## JavaScript: Typumwandlung und ihre Bedeutung in JavaScript

In JavaScript gibt es verschiedene Möglichkeiten der Typumwandlung, um Werte zwischen verschiedenen Datentypen zu konvertieren. Dies ist wichtig, um Operationen durchzuführen oder Vergleiche zwischen verschiedenen Typen durchzuführen. Im Folgenden sind einige grundlegende Konzepte und Codebeispiele zur Typumwandlung in JavaScript:

### Beispiel 1: Implizite Typumwandlung

```javascript
// Implizite Typumwandlung
const num = 10 + ""; // num ist jetzt ein String "10"
const bool = true + 1; // bool ist jetzt 2, da true implizit zu 1 umgewandelt wird
```

In diesem Beispiel werden Zahlen und Booleans implizit in Strings und Zahlen umgewandelt, um Operationen durchzuführen.

### Beispiel 2: Explizite Typumwandlung

```javascript
// Explizite Typumwandlung
const str = String(123); // str ist jetzt ein String "123"
const num = Number("123"); // num ist jetzt eine Zahl 123
const bool = Boolean(0); // bool ist jetzt false, da 0 als falsy gilt
```

Hier werden explizite Typumwandlungen mithilfe von String(), Number() und Boolean() durchgeführt, um Werte in die gewünschten Datentypen umzuwandeln.

### Beispiel 3: Vergleich und Gleichheit

```javascript
// Vergleich und Gleichheit
console.log(5 == "5"); // true, da JavaScript die Werte vor dem Vergleich umwandelt
console.log(5 === "5"); // false, da der strenge Gleichheitsoperator keine Typumwandlung durchführt
```

Hier wird der Unterschied zwischen dem lose und streng Gleichheitsoperator gezeigt. Der lose Gleichheitsoperator (==) führt vor dem Vergleich eine Typumwandlung durch, während der strenge Gleichheitsoperator (===) dies nicht tut.