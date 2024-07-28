# JavaScript: Verzweigungen und bedingte Anweisungen in JavaScript

JavaScript bietet verschiedene Möglichkeiten, um Verzweigungen und bedingte Anweisungen zu implementieren. Diese ermöglichen es, Codebedingungen zu prüfen und unterschiedliche Aktionen basierend auf diesen Bedingungen auszuführen. Im Folgenden sind einige grundlegende Konzepte und Codebeispiele für Verzweigungen und bedingte Anweisungen in JavaScript:

## Beispiel 1: if-Anweisung

```javascript
let zahl = 10;

if (zahl > 0) {
  console.log('Die Zahl ist positiv');
} else if (zahl === 0) {
  console.log('Die Zahl ist Null');
} else {
  console.log('Die Zahl ist negativ');
}
```

Die if-Anweisung ermöglicht es, einen Codeblock auszuführen, wenn eine Bedingung wahr ist. Mit else if können zusätzliche Bedingungen überprüft werden, während else einen Standardcodeblock definiert, der ausgeführt wird, wenn keine der vorherigen Bedingungen zutrifft.

```javascript
let tag = 'Montag';

switch (tag) {
  case 'Montag':
    console.log('Heute ist Montag');
    break;
  case 'Dienstag':
    console.log('Heute ist Dienstag');
    break;
  default:
    console.log('Heute ist kein bekannter Wochentag');
}
```

Die switch-Anweisung ermöglicht es, eine Vielzahl von Bedingungen zu überprüfen und basierend darauf verschiedene Aktionen auszuführen. Jeder case-Block entspricht einem möglichen Wert der geprüften Variable.

## Beispiel 3: Ternärer Operator

```javascript
let alter = 20;
let status = (alter >= 18) ? 'Volljährig' : 'Minderjährig';
console.log(status);
```

Der ternäre Operator (? :) ermöglicht es, eine Bedingung in einem einzigen Ausdruck auszuwerten. Wenn die Bedingung wahr ist, wird der Ausdruck vor dem : ausgeführt, andernfalls der Ausdruck danach.