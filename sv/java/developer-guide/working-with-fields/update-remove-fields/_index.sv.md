---
title: Uppdatera, ta bort fält
type: docs
weight: 20
url: /sv/java/update-remove-fields/
description: Det här avsnittet förklarar hur du uppdaterar eller tar bort fält.
---
## **Uppdatera fält**
 Aspose.Diagram for .NET låter dig uppdatera och ta bort[fält](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) till Microsoft Visio diagram från dina egna applikationer, utan Microsoft Office Automation.

 De[Fält](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) objekt representerar textfält i en[text](https://reference.aspose.com/diagram/java/com.aspose.diagram/text) springa. Fältegenskapen, exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass stöder en samling Aspose.Diagram.Field-objekt.
### **Programmeringsexempel**
Följande koduppdateringsfält i form.
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

### **Ta bort fält**
Följande kodbit tar bort fält i form.
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

