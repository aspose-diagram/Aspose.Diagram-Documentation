---
title: Mettre à jour, supprimer des champs
type: docs
weight: 20
url: /fr/net/update-remove-fields/
description: Cette section explique comment mettre à jour ou supprimer des champs.
---
## **Mettre à jour le champ**
 Aspose.Diagram for .NET vous permet de mettre à jour et de supprimer[champ](https://reference.aspose.com/diagram/net/aspose.diagram/field) aux schémas Microsoft Visio à partir de vos propres applications, sans Microsoft Office Automation.

 La[Champ](https://reference.aspose.com/diagram/net/aspose.diagram/field) l'objet représente un champ de texte dans un[texte](https://reference.aspose.com/diagram/net/aspose.diagram/text) Cours. La propriété du terrain, exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) prend en charge une collection d'objets Aspose.Diagram.Field.
### **Exemple de programmation**
Le morceau suivant de champ de mise à jour de code dans shape.
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UpdateField();

// Create a new diagram
// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

//Get Visio Shape
Shape shape = page.Shapes[0];
//Get field
Field fld = shape.Fields[0];
//Update format of field
fld.Format.Val = "";
fld.Format.Ufev.Unit = MeasureConst.Undefined;
fld.Format.Ufev.F = "";

//Update value of field
fld.Value.Val = "1";
fld.Value.Ufev.F = "";
fld.Value.Ufev.Unit = MeasureConst.Undefined;

// Save diagram 
diagram.Save(dataDir + "UpdateField_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

### **Supprimer le champ**
Le morceau de code suivant supprime le champ dans la forme.
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_RemoveField();

// Create a new diagram
// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

//Get Visio Shape
Shape shape = page.Shapes[0];
//Get field
Field fld = shape.Fields[0];
//Remove field
shape.Fields.Remove(fld);

// Save diagram 
diagram.Save(dataDir + "RemoveField_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
