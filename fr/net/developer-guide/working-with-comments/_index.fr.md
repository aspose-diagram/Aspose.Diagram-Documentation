---
title: Travailler avec des commentaires
type: docs
weight: 220
url: /fr/net/working-with-comments/
description: Cette page décrit comment ajouter ou modifier des commentaires avec la bibliothèque Aspose.Diagram.
---
## **Ajouter un commentaire au niveau de la page dans le Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API permet aux développeurs de placer des commentaires n'importe où dans la page de dessin Visio.
### **Ajouter un commentaire**
 La méthode AddComment, exposée par le[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) classe, permet aux développeurs d'ajouter des commentaires à une page de dessin. Il prend les coordonnées X et Y avec une chaîne de commentaire.
#### **Ajouter un commentaire Exemple de programmation**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioComments();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add comment
diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

// Save diagram
diagram.Save(dataDir + "AddComment_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Modifier un commentaire au niveau de la page dans le Visio Diagram**
 Les utilisateurs Microsoft Visio ajoutent des commentaires à la page entière qui sont présentés par une icône dans le coin supérieur gauche de la page. Les développeurs peuvent[ajouter des commentaires au niveau de la page dans le Visio](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API prend également en charge la modification du commentaire au niveau de la page dans le Visio.
### **Modifier le commentaire**
 La propriété Comment, exposée par le[Annotation](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) classe, permet aux développeurs de modifier les commentaires dans la page de dessin Visio.
#### **Éditer un exemple de programmation de commentaire**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioComments();

// Load Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get collection of the annotations
AnnotationCollection annotations = diagram.Pages.GetPage("Page-1").PageSheet.Annotations;

// Iterate through the annotations
foreach (Annotation annotation in annotations)
{
    string comment = annotation.Comment.Value;
    comment += "Updation mark";
    annotation.Comment.Value = comment;
}
// Save Visio
diagram.Save(dataDir + "EditComment_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Ajouter un commentaire au niveau de la forme dans le dessin Visio**
[Aspose.Diagram for .NET](https://www.aspose.com/products/diagram/net)API permet aux développeurs d'ajouter des commentaires à la forme dans un dessin Visio.
### **Ajouter un commentaire**
Une méthode AddComment surchargée, exposée par le[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page)La classe prend une instance de classe Shape et la chaîne de texte du commentaire.
#### **Ajouter un commentaire Exemple de programmation**
**C#**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// retrieve page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(12);

page.AddComment(shape, "Hello");

// save diagram

diagram.Save(@"c:\temp\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
