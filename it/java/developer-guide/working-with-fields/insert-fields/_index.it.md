---
title: Crea, Inserisci campi
type: docs
weight: 10
url: /it/java/create-insert-fields/
description: Come creare, inserire campi utilizzando Java Diagram API .
---
## **Inserisci campo**
 Aspose.Diagram for Java consente di creare e inserire[campo](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) a Microsoft Visio diagrammi dall'interno delle proprie applicazioni, senza Microsoft Office Automazione.
### **Esempio di programmazione**
```
{{< highlight "java" >}}
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
```

