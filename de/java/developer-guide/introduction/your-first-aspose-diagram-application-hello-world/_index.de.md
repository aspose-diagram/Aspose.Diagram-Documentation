---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /de/java/your-first-aspose-diagram-application-hello-world/
description: Auf dieser Seite wird beschrieben, wie Sie die erste Anwendung mit der Bibliothek Aspose.Diagram erstellen.
---
{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1.  Erstellen Sie eine Instanz der[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Klasse.
1.  Wenn Sie eine Lizenz haben, dann[Wende es an](https://reference.aspose.com/diagram/java/com.aspose.diagram/License).
 Wenn Sie die Evaluierungsversion verwenden, überspringen Sie die lizenzbezogenen Codezeilen.
1. Erstellen Sie eine neue Visio-Datei oder öffnen Sie eine vorhandene Visio-Datei.
1. Erstellen Sie ein neues Textfeld.
1.  Füge die Wörter ein**Hello World!** in ein Textfeld.
1. Generieren Sie die geänderte Datei Microsoft Visio.

Die Implementierung der obigen Schritte wird in den folgenden Beispielen demonstriert.

### **Codebeispiel: Erstellen einer neuen Diagram**

The following example creates a new diagram from the scratch, writes Hello World! on the first page and saves the Visio file.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-CreateNewVisio-CreateNewVisio.java" >}}

### **Codebeispiel: Öffnen einer vorhandenen Datei**

The following example opens an existing Microsoft Visio template file named "Sample.vsdx", inputs "Hello World!" text in the first page and saves the diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ReadVisioDiagram-ReadVisioDiagram.java" >}}
