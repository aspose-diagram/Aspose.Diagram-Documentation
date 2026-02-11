---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /de/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

This beginner's topic shows how developers can create a simple first application (Hello World) using Aspose.Diagram' simple API. The application creates a Microsoft Visio file with the words Hello World in the page.

{{% /alert %}}

### **Creating the Hello World Application**

To create the Hello World application using Aspose.Diagram API:

1. Erstellen Sie eine Instanz der Workbook-Klasse.
1. Wenden Sie die Lizenz an:
 1. Wenn Sie eine Lizenz erworben haben, verwenden Sie die Lizenz in Ihrer Anwendung, um Zugriff auf die volle Funktionalität von Aspose.Diagram zu erhalten
 1. Wenn Sie die Evaluierungsversion der Komponente verwenden (wenn Sie Aspose.Diagram ohne Lizenz verwenden), überspringen Sie diesen Schritt.
1. Erstellen Sie eine neue Microsoft Visio-Datei oder öffnen Sie eine vorhandene Datei, in der Sie Text hinzufügen/aktualisieren möchten.
1.  Füge die Wörter ein**Hello World!** in die aufgerufene Seite.
1. Generieren Sie die geänderte Datei Microsoft Visio.

Die folgenden Beispiele veranschaulichen die obigen Schritte.

#### **Erstellen einer Diagram**

The following example creates a new diagram from scratch, writes the words "Hello World!" on the first page, and saves the file.

**Erstellen Sie eine neue visio-Datei** 

![todo: Bild_alt_Text](your-first-aspose-diagram-application-hello-world_1.png)


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


#### **Öffnen einer bestehenden Datei**

The following example opens an existing Microsoft Visio template file, writes the words "Hello World!" in the first page, and saves the diagram as a new file.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

diagram = Diagram(os.path.join(sourceDir, "Basic Shapes.vss"))

#// Add a new hello world rectangle shape
shapeId = diagram.add_shape(4.25, 5.5, 2, 1, "Rectangle", 0)
shape = diagram.pages[0].shapes.get_shape(shapeId)
shape.text.value.add(Txt("Hello World"))

#// Save diagram in the VSDX format
diagram.save("CreateHelloWorldVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}

