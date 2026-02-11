---
title: Créer, Insérer des champs
type: docs
weight: 10
url: /fr/java/create-insert-fields/
description: Comment créer, insérer des champs en utilisant Java Diagram API .
---
## **Insérer un champ**
 Aspose.Diagram for Java vous permet de créer et d'insérer[champ](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) aux schémas Microsoft Visio à partir de vos propres applications, sans Microsoft Office Automation.
### **Exemple de programmation**
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

