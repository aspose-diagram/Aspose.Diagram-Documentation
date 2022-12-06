---
title: Aspose.Diagram für Node.js-Beispiele
type: docs
weight: 10
url: /de/java/aspose-diagram-for-node-js-examples/
description: Mit Viso Diagram Node.js API können Sie mit Visio-Diagrammen arbeiten, ohne das zugrunde liegende Dateiformat zu verstehen. Sie können Visio-VSDX-Dateien von Grund auf neu erstellen und VSDX-Dateien mit nur wenigen Codezeilen in PNG konvertieren.
---
Aspose.Diagram für Node.js ist einfach zu verwenden und lässt Sie mit Visio-Diagrammen arbeiten, ohne das zugrunde liegende Dateiformat zu verstehen. Sie können Visio VSDX-Dateien mit einfachen Codezeilen von Grund auf neu erstellen. Sie können auch VSDX-Dateien mit nur wenigen Codezeilen in PNG konvertieren. In diesem Artikel führen wir einige grundlegende Beispiele für die Arbeit mit Visio VSDX-Dateien unter Verwendung von Aspose.Diagram für Node.js API auf.
## **Erstellen Sie Visio VSDX von Grund auf mit Node.js**
{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

var diagram = new aspose.diagram.Diagram();

diagram.save("output.vsdx", aspose.diagram.SaveFileFormat.VSDX);

{{< /highlight >}}
## **Seite der Datei Visio VSDX in das PNG-Format exportieren**
{{< highlight "java" >}}

 var aspose = aspose || {};

aspose.diagram = require("aspose.diagram");

diagram = new aspose.diagram.Diagram("template.vsdx");

// Save diagram as PNG

options = new aspose.diagram.ImageSaveOptions(aspose.diagram.SaveFileFormat.PNG);

// Save one page only, by page index

options.setPageIndex(0);

// Save resultant Image file

diagram.save("output.png", options);

{{< /highlight >}}
