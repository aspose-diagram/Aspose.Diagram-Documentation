---
title: Crear, Insertar campos
type: docs
weight: 10
url: /es/java/create-insert-fields/
description: Cómo crear, inserte campos usando Java Diagram API .
---
## **Insertar campo**
 Aspose.Diagram for Java le permite crear e insertar[campo](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) a Microsoft Visio diagramas desde dentro de sus propias aplicaciones, sin Microsoft Office Automatización.
### **Ejemplo de programación**

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


