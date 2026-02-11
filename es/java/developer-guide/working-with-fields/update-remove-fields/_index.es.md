---
title: Actualizar, eliminar campos
type: docs
weight: 20
url: /es/java/update-remove-fields/
description: Esta sección explica cómo actualizar o eliminar campos.
---
## **Actualizar campo**
 Aspose.Diagram for .NET le permite actualizar y eliminar[campo](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) a Microsoft Visio diagramas desde dentro de sus propias aplicaciones, sin Microsoft Office Automatización.

 los[Campo](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) objeto representa un campo de texto en un[texto](https://reference.aspose.com/diagram/java/com.aspose.diagram/text) correr. La propiedad de campo, expuesta por la[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La clase admite una colección de objetos Aspose.Diagram.Field.
### **Ejemplo de programación**
El siguiente fragmento de código actualiza el campo en forma.

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


### **Eliminar campo**
El siguiente fragmento de código elimina el campo en forma.

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


