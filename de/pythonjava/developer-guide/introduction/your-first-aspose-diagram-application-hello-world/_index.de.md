---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /de/python-java/your-first-aspose-diagram-application-hello-world/
description: Auf dieser Seite wird beschrieben, wie Sie die erste Anwendung mit der Bibliothek Aspose.Diagram erstellen.
---
{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1. Erstellen Sie eine Instanz der Klasse Diagram.
1. Wenden Sie die Lizenz an:
 1. Wenn Sie eine Lizenz erworben haben, verwenden Sie die Lizenz in Ihrer Anwendung, um Zugriff auf die volle Funktionalität von Aspose.Diagram zu erhalten
 1. Wenn Sie die Evaluierungsversion der Komponente verwenden (wenn Sie Aspose.Diagram ohne Lizenz verwenden), überspringen Sie diesen Schritt.
1. Erstellen Sie eine neue Visio-Datei oder öffnen Sie eine vorhandene Visio-Datei.
1. Erstellen Sie ein neues Textfeld.
1.  Füge die Wörter ein**Hello World!** in ein Textfeld.
1. Generieren Sie die geänderte Datei Microsoft Visio.

Die Implementierung der obigen Schritte wird in den folgenden Beispielen demonstriert.

### **Code Sample: Creating a New Diagram and Writing Hello World!**

Das folgende Beispiel öffnet eine vorhandene Microsoft Visio-Vorlagendatei mit dem Namen "[Basic_Shapes.vss](Basic_Shapes.vss)", inputs "Hello World!" text in the first page and saves the diagram.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-CreatingHelloWorldVisioFile.py" >}}
