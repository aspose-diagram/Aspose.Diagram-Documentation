---
title: Créer, Insérer des champs
type: docs
weight: 10
url: /fr/net/create-insert-fields/
description: Comment créer, insérer des champs en utilisant C# Diagram API .
---
## **Insérer un champ**
 Aspose.Diagram for .NET vous permet de créer et d'insérer[champ](https://reference.aspose.com/diagram/net/aspose.diagram/field) aux schémas Microsoft Visio à partir de vos propres applications, sans Microsoft Office Automation.
### **Exemple de programmation**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_InsertField();

// Create a new diagram
// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

//Get Visio Shape
Shape shape = page.Shapes[0];
//Insert field
Field fld = new Field();
fld.Value.Val = "1";
shape.Fields.Add(fld);

// Save diagram 
diagram.Save(dataDir + "InsertField_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
