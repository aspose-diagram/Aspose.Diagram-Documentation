---
title: Mettre à jour, supprimer des champs
type: docs
weight: 20
url: /fr/java/update-remove-fields/
description: Cette section explique comment mettre à jour ou supprimer des champs.
---
## **Mettre à jour le champ**
 Aspose.Diagram for .NET vous permet de mettre à jour et de supprimer[champ](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) aux schémas Microsoft Visio à partir de vos propres applications, sans Microsoft Office Automation.

 La[Champ](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) l'objet représente un champ de texte dans un[texte](https://reference.aspose.com/diagram/java/com.aspose.diagram/text) Cours. La propriété du terrain, exposée par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) prend en charge une collection d'objets Aspose.Diagram.Field.
### **Exemple de programmation**
Le morceau suivant de champ de mise à jour de code dans shape.
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

### **Supprimer le champ**
Le morceau de code suivant supprime le champ dans la forme.
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

