---
title: Dokument Visio programmgesteuert erstellen
linktitle: Dokument Visio erstellen
type: docs
weight: 10
url: /de/java/create-visio-document/
description: Auf dieser Seite wird beschrieben, wie Sie ein Visio-Dokument von Grund auf mit der Aspose.Diagram-Bibliothek erstellen.
---
## **Erstellen einer neuen Visio-Zeichnung**
Mit Aspose.Diagram for Java können Sie Microsoft Visio Diagramme aus Ihren eigenen Anwendungen lesen und erstellen, ohne Microsoft Office Automatisierung. Der erste Schritt beim Erstellen neuer Dokumente besteht darin, eine diagram zu erstellen. Fügen Sie dann Formen und Verbinder hinzu, um die diagram aufzubauen.
### **Programmierbeispiel Visio Zeichnen erstellen**
Der folgende Code zeigt, wie eine neue Microsoft Visio-Zeichnung erstellt wird. Bitte beachten Sie, dass die leere Zeichnung eine einzelne leere Seite enthält.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}} 

Das Zeichenpapierformat ist standardmäßig Letter.

{{% /alert %}} 

