## JavaScript: Zugriff auf HTML mit dem Document Object Model (DOM)

Das Document Object Model (DOM) ist eine Programmierschnittstelle, die es JavaScript ermöglicht, auf HTML- und XML-Dokumente zuzugreifen und diese zu verändern. Dadurch können Webentwickler dynamische und interaktive Webseiten erstellen. Im Folgenden sind einige grundlegende Konzepte und Codebeispiele zum Zugriff auf HTML-Elemente mit dem DOM:

### Beispiel 1: Zugriff auf ein HTML-Element

```html
<!DOCTYPE html>
<html>
<head>
  <title>DOM Beispiel</title>
</head>
<body>

<h1 id="headline">Willkommen!</h1>

<script>
  // Zugriff auf das HTML-Element mit der ID "headline"
  const headlineElement = document.getElementById('headline');
  // Ändern des Textinhalts des Elements
  headlineElement.textContent = 'Hallo Welt!';
</script>

</body>
</html>
```

In diesem Beispiel wird das HTML-Element mit der ID "headline" über document.getElementById() ausgewählt und der Textinhalt mit textContent geändert.

### Beispiel 2: Ereignisbehandlung

```html
<!DOCTYPE html>
<html>
<head>
  <title>DOM Ereignisbehandlung</title>
</head>
<body>

<button id="myButton">Klick mich!</button>

<script>
  // Zugriff auf das HTML-Element mit der ID "myButton"
  const button = document.getElementById('myButton');
  // Hinzufügen eines Klick-Ereignislisteners
  button.addEventListener('click', function() {
    alert('Button wurde geklickt!');
  });
</script>

</body>
</html>
```

Hier wird ein Ereignislistener hinzugefügt, um auf Klickereignisse des Buttons zu reagieren und eine Benachrichtigung anzuzeigen.

### Beispiel 3: Manipulation von HTML-Elementen

```html
<!DOCTYPE html>
<html>
<head>
  <title>DOM Manipulation</title>
</head>
<body>

<div id="container">
  <p>Dies ist ein Absatz.</p>
</div>

<script>
  // Zugriff auf das HTML-Element mit der ID "container"
  const container = document.getElementById('container');
  // Hinzufügen eines neuen Absatzes
  const newParagraph = document.createElement('p');
  newParagraph.textContent = 'Ein weiterer Absatz.';
  // Einfügen des neuen Absatzes in den Container
  container.appendChild(newParagraph);
</script>

</body>
</html>
```

In diesem Beispiel wird ein neuer Absatz erstellt und dem HTML-Element mit der ID "container" hinzugefügt.