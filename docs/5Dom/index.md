# 5 DOM

Gliederung

[5.1 Einführung in das Document Object Model](5.1_Einfuehrung_in_das_Document_Object_Model.md)<br>
[5.2 Grundlagen von DOM](5.2_Grundlagen_von_DOM.md)<br>
[5.3 Navigieren im DOM-Baum](5.3_Navigieren_im_DOM_Baum.md)<br>
[5.4 Anwendungsbeispiele](5.4_Anwendungsbeispiele.md)<br>
[5.5 Selbsttest und Zusammenfasssung zum gesamten Kapitel DOM](5.5_Selbsttest_und_Zusammenfassung_zum_gesamten_Kapitel_DOM.md)<br>

## Was ist das DOM?

Das **Document Object Model (DOM)** ist eine plattform- und sprachunabhängige Schnittstelle, die uns den Zugriff auf den Inhalt, die Struktur und den Stil von (HTML-)Dokumenten ermöglicht. Es erlaubt, dynamische Änderungen vorzunehmen und die Ergebnisse direkt in die ursprüngliche Darstellung des Dokuments zu integrieren.

**HTML-Elemente** sind in einer **hierarchischen Baumstruktur** organisiert. Jedes Element des Dokuments, sei es ein HTML-Tag, ein Attribut oder ein Text, wird im DOM als Knoten repräsentiert. Diese Knoten sind hierarchisch angeordnet, mit einem Wurzelknoten, der das gesamte Dokument repräsentiert. Das DOM macht es möglich, auf diese Knoten zuzugreifen und sie zu manipulieren.

Da Browser objektorientiert programmiert sind, können wir mit JavaScript auf die hierarchischen Bestandteile eines HTML-Dokuments objektorientiert zugreifen. Das DOM stellt eine standardisierte API bereit, um HTML und XML zu manipulieren. Diese API ist für Webentwickler von zentraler Bedeutung, da fast jede interaktive Webseite Änderungen am DOM erfordert.

## Warum ist das DOM wichtig?

Das DOM bildet die Grundlage für nahezu alle interaktiven und dynamischen Funktionen im Web. Egal, ob wir:

- Inhalte dynamisch hinzufügen oder entfernen,

- die Darstellung von Elementen ändern (z. B. CSS-Styles),

- Benutzerinteraktionen verarbeiten (z. B. Klick-Events),

- oder komplexe Animationen implementieren möchten – das DOM ist dabei unser Werkzeug.

Ein Verständnis des DOM ist daher für jede:n Webentwickler:in unverzichtbar.

## Beispiel: DOM-Baum

Ein einfaches HTML-Dokument könnte wie folgt in einem DOM-Baum repräsentiert werden:

```html linenums="1" hl_lines="6"
<html>
  <head>
    <title>Meine tolle Seite</title>
  </head>
  <body>
    <h1 id="beispiel">Willkommen!</h1>
    <p>Dies ist ein Beispiel.</p>
  </body>
</html>
```

Hierbei stellt `<html>` die Wurzel dar, die wiederum die Knoten `<head>` und `<body>` enthält. Diese Struktur bildet die Grundlage für die hierarchische Navigation im DOM.

### Zugriff auf das DOM mit JavaScript

Mit JavaScript können wir auf Elemente im DOM zugreifen und sie manipulieren. Zum Beispiel:

```javascript linenums="1" hl_lines="1"
let element = document.getElementById('beispiel');

// Ändern des Inhalts
element.textContent = 'Moin';
```

### Was passiert in diesem Beispiel?

1. **HTML-Dokument (DOM-Baum)**:

    - Das `<html>`-Element ist der Wurzelknoten des DOM-Baumes.

    - Das `<body>`-Element ist ein Kindknoten von `<html>` und enthält die sichtbaren Inhalte.

        - Ein `<h1>`-Element mit der ID `beispiel` und dem Text "Willkommen!".

2. **JavaScript-Code**:

    - **`document.getElementById('beispiel')`**:

        - Diese Methode sucht im DOM-Baum nach einem Element mit der ID `beispiel`.

        - Das `<h1>`-Element wird gefunden und der Variable `element` zugewiesen.

    - **`element.textContent = 'Moin';`**:

        - Die Eigenschaft `textContent` des `<h1>`-Elements wird geändert.

        - Der ursprüngliche Text "Willkommen!" wird durch "Moin" ersetzt.


Wir nutzen Methoden wie `getElementById`, `querySelector` oder `getElementsByClassName`, um spezifische Elemente auszuwählen. Diese ermöglichen uns, Inhalte, Attribute oder Stile der Elemente zu ändern.

<figure>
  <video controls width="600">
    <source src="media/DOM.mp4" type="video/mp4">
    Unser Browser unterstützt das Video-Tag nicht.
  </video>
  <figcaption>Video zur Einführung in DOM (1:50 Minuten)</figcaption>
</figure>

In diesem Kapitel werden die Grundlagen des DOM, die Navigation im DOM-Baum und praktische Anwendungsbeispiele behandelt.
