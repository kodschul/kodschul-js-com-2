## JavaScript: Iteration durch Arrays und Objekte in JavaScript

In JavaScript gibt es verschiedene Methoden, um durch Arrays und Objekte zu iterieren. Dies ermöglicht es, Elemente zu durchlaufen und Aktionen für jedes Element auszuführen. Im Folgenden sind einige grundlegende Konzepte und Codebeispiele zur Iteration durch Arrays und Objekte in JavaScript:

### Iteration durch Arrays

#### Beispiel 1: Verwendung von for-Schleifen

```javascript
const fruits = ['Apfel', 'Banane', 'Orange'];

for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}
```

Die for-Schleife ist eine traditionelle Methode, um durch Arrays zu iterieren. Sie verwendet einen Zähler (in diesem Fall i), um jedes Element im Array nacheinander zu durchlaufen.

#### Beispiel 2: Verwendung von forEach()

```javascript
const numbers = [1, 2, 3, 4, 5];

numbers.forEach((number) => {
  console.log(number);
});
```

Die forEach()-Methode ruft eine Funktion für jedes Element im Array auf. Sie ist eine elegante und moderne Methode, um durch Arrays zu iterieren.

### Iteration durch Objekte
#### Beispiel 3: Verwendung von for...in-Schleifen

```javascript
const person = {
  name: 'John',
  age: 30,
  city: 'Berlin'
};

for (let key in person) {
  console.log(key + ': ' + person[key]);
}
```

Die for...in-Schleife wird verwendet, um durch die Eigenschaften eines Objekts zu iterieren. Sie ruft den Namen jeder Eigenschaft des Objekts ab.

#### Beispiel 4: Verwendung von Object.keys()

```javascript
const person = {
  name: 'John',
  age: 30,
  city: 'Berlin'
};

Object.keys(person).forEach((key) => {
  console.log(key + ': ' + person[key]);
});
```

Die Object.keys()-Methode gibt ein Array mit den Schlüsseln eines Objekts zurück. Sie kann zusammen mit forEach() verwendet werden, um durch die Schlüssel des Objekts zu iterieren und auf die zugehörigen Werte zuzugreifen.