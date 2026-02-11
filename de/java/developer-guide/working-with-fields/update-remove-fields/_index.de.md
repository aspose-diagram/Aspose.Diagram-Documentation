---
title: Felder aktualisieren, entfernen
type: docs
weight: 20
url: /de/java/update-remove-fields/
description: In diesem Abschnitt wird erläutert, wie Sie Felder aktualisieren oder entfernen.
---
## **Feld aktualisieren**
 Aspose.Diagram for .NET lässt Sie aktualisieren und entfernen[aufstellen](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) bis Microsoft Visio Diagramme aus eigenen Applikationen, ohne Microsoft Office Automatisierung.

 Das[Aufstellen](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) Objekt repräsentiert ein Textfeld in a[Text](https://reference.aspose.com/diagram/java/com.aspose.diagram/text) Lauf. Die Feldeigenschaft, die durch die verfügbar gemacht wird[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) -Klasse unterstützt eine Sammlung von Aspose.Diagram.Field-Objekten.
### **Programmierbeispiel**
Das folgende Stück Codeaktualisierungsfeld in Form.

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}


### **Feld entfernen**
Der folgende Codeabschnitt entfernt das Feld in der Form.

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}


