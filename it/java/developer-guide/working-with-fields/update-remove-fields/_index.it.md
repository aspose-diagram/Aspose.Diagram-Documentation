---
title: Aggiorna, rimuovi campi
type: docs
weight: 20
url: /it/java/update-remove-fields/
description: Questa sezione spiega come aggiornare o rimuovere i campi.
---
## **Aggiorna Campo**
 Aspose.Diagram for .NET consente di aggiornare e rimuovere[campo](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) a Microsoft Visio diagrammi dall'interno delle proprie applicazioni, senza Microsoft Office Automazione.

 Il[Campo](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) l'oggetto rappresenta il campo di testo in a[testo](https://reference.aspose.com/diagram/java/com.aspose.diagram/text) correre. La proprietà del campo, esposta dal[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class supporta una raccolta di oggetti Aspose.Diagram.Field.
### **Esempio di programmazione**
Il seguente pezzo di campo di aggiornamento del codice in forma.

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


### **Rimuovi campo**
Il seguente pezzo di codice rimuove il campo in shape.

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


