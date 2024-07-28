# JavaScript: Scope - Gültigkeitsbereich von Variablen verstehen

Der Scope in JavaScript bestimmt, wo Variablen und Funktionen in Ihrem Code verfügbar sind. Es ist wichtig, den Scope zu verstehen, um Probleme mit Variablenzuweisungen und Funktionsaufrufen zu vermeiden. Im Folgenden werden die verschiedenen Arten von Scopes in JavaScript erläutert:

## Globaler Scope

Variablen und Funktionen, die außerhalb von Funktionen definiert sind, haben einen globalen Scope und sind im gesamten Programm verfügbar.

```javascript
// Globale Variable
var globalVariable = 'Ich bin global';

function testFunction() {
  console.log(globalVariable); // Ausgabe: Ich bin global
}

testFunction();
```

## Lokaler Scope
Variablen, die innerhalb einer Funktion mit var, let oder const deklariert werden, haben einen lokalen Scope und sind nur innerhalb dieser Funktion sichtbar.

```javascript
function testFunction() {
  var localVariable = 'Ich bin lokal';
  console.log(localVariable); // Ausgabe: Ich bin lokal
}

testFunction();
console.log(localVariable); // Fehler: localVariable ist nicht definiert
```

## Block Scope
Variablen, die mit let oder const innerhalb eines Blocks ({}) deklariert werden, haben einen Block Scope und sind nur innerhalb dieses Blocks sichtbar.

```javascript
{
  let blockVariable = 'Ich bin ein Block';
  console.log(blockVariable); // Ausgabe: Ich bin ein Block
}

console.log(blockVariable); // Fehler: blockVariable ist nicht definiert
```

## Scope-Ketten
JavaScript verwendet eine Scope-Kette, um nach Variablen zu suchen. Wenn eine Variable in einer Funktion nicht gefunden wird, sucht JavaScript in der umgebenden Funktion und dann im globalen Scope.

```javascript
var globalVar = 'Global';

function outerFunction() {
  var outerVar = 'Outer';

  function innerFunction() {
    var innerVar = 'Inner';
    console.log(innerVar); // Ausgabe: Inner
    console.log(outerVar); // Ausgabe: Outer
    console.log(globalVar); // Ausgabe: Global
  }

  innerFunction();
}

outerFunction();
```