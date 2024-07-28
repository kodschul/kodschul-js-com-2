## JavaScript Formio: Formulardaten und Validierung

Form.io ist eine leistungsstarke Plattform zur Erstellung und Verwaltung von Formularen in Webanwendungen. Mit Formio können komplexe Formulare erstellt und Formulardaten effizient verwaltet und validiert werden. Im Folgenden sind einige grundlegende Konzepte und Techniken zur Arbeit mit Formio beschrieben:

### Grundlagen von Formio

Formio bietet eine Vielzahl von Funktionen, um benutzerdefinierte Formulare zu erstellen und zu verwalten. Es stellt sowohl eine visuelle Formbuilder-Oberfläche als auch eine robuste JavaScript-API zur Verfügung.

#### 1. Installation

Formio kann über npm installiert und in einer Webanwendung verwendet werden.

```bash
npm install --save formiojs
```

#### 2. Erstellung eines Formulars
Ein einfaches Formular kann mit der Formio-API erstellt und gerendert werden.

```javascript
import { Formio } from 'formiojs';

// Formular-Definition
const formDefinition = {
  components: [
    {
      type: 'textfield',
      key: 'name',
      label: 'Name',
      placeholder: 'Geben Sie Ihren Namen ein',
      input: true
    },
    {
      type: 'email',
      key: 'email',
      label: 'Email',
      placeholder: 'Geben Sie Ihre Email ein',
      input: true
    },
    {
      type: 'button',
      action: 'submit',
      label: 'Submit',
      theme: 'primary'
    }
  ]
};

// Formular rendern
Formio.createForm(document.getElementById('formio'), formDefinition).then((form) => {
  form.on('submit', (submission) => {
    console.log('Formulardaten:', submission);
  });
});

```

In diesem Beispiel wird ein einfaches Formular mit einem Textfeld, einem E-Mail-Feld und einer Schaltfläche erstellt und gerendert.

### Formulardaten verwalten
Formio bietet verschiedene Methoden zum Verwalten und Bearbeiten von Formulardaten.

1. Formulardaten abrufen
Die Daten eines Formulars können mit der submission-Eigenschaft des Formularobjekts abgerufen werden.

```javascript
form.submission.then((submission) => {
  console.log('Aktuelle Formulardaten:', submission.data);
});
```

2. Formulardaten setzen
Die Daten eines Formulars können mit der submission-Eigenschaft des Formularobjekts gesetzt werden

```javascript
form.submission = {
  data: {
    name: 'Max Mustermann',
    email: 'max@mustermann.de'
  }
};
```

### Validierung von Formulardaten
Formio bietet umfangreiche Validierungsfunktionen, um sicherzustellen, dass die eingegebenen Daten den definierten Anforderungen entsprechen.

1. Eingebaute Validierungen
Jedes Feld im Formular kann mit eingebauten Validierungsregeln versehen werden, wie z.B. erforderliche Felder, Musterüberprüfung und Längenbeschränkungen.

```javascript
const formDefinition = {
  components: [
    {
      type: 'textfield',
      key: 'name',
      label: 'Name',
      placeholder: 'Geben Sie Ihren Namen ein',
      input: true,
      validate: {
        required: true,
        minLength: 3
      }
    },
    {
      type: 'email',
      key: 'email',
      label: 'Email',
      placeholder: 'Geben Sie Ihre Email ein',
      input: true,
      validate: {
        required: true,
        pattern: '^\\S+@\\S+$'
      }
    }
  ]
};
```

In diesem Beispiel wird das Namensfeld als erforderlich definiert und muss mindestens drei Zeichen lang sein. Das E-Mail-Feld ist ebenfalls erforderlich und muss einem bestimmten Muster entsprechen.

2. Benutzerdefinierte Validierungen
Formio ermöglicht es auch, benutzerdefinierte Validierungslogik zu implementieren, um spezifische Anforderungen zu erfüllen.

```javascript
const formDefinition = {
  components: [
    {
      type: 'textfield',
      key: 'name',
      label: 'Name',
      placeholder: 'Geben Sie Ihren Namen ein',
      input: true,
      validate: {
        required: true,
        custom: 'valid = input === "Max Mustermann" ? true : "Nur Max Mustermann ist erlaubt";'
      }
    }
  ]
};
```

In diesem Beispiel wird eine benutzerdefinierte Validierung implementiert, die nur den Namen "Max Mustermann" erlaubt.