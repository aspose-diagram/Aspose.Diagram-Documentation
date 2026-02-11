---
title: Arbeiten mit Kommentaren
type: docs
weight: 220
url: /de/net/working-with-comments/
description: Auf dieser Seite wird beschrieben, wie Sie Kommentare mit der Bibliothek Aspose.Diagram hinzufügen oder bearbeiten.
---
## **Fügen Sie einen Kommentar auf Seitenebene in Visio hinzu**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API ermöglicht Entwicklern das Platzieren von Kommentaren überall auf der Zeichenseite Visio.
### **Einen Kommentar hinzufügen**
 Die AddComment-Methode, verfügbar gemacht durch die[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) -Klasse ermöglicht Entwicklern das Hinzufügen von Kommentaren zu einem Zeichenblatt. Es nimmt die X- und Y-Koordinaten zusammen mit einer Kommentarzeichenfolge.
#### **Programmierbeispiel Kommentar hinzufügen**

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

## **Bearbeiten Sie einen Kommentar auf Seitenebene im Visio Diagram**
 Microsoft Visio Benutzer fügen der gesamten Seite Kommentare hinzu, die durch ein Symbol in der oberen linken Ecke der Seite angezeigt werden. Entwickler können[Kommentare auf Seitenebene in Visio hinzufügen](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API unterstützt zusätzlich das Ändern des Kommentars auf Seitenebene in Visio.
### **Kommentar bearbeiten**
 Die Comment-Eigenschaft, verfügbar gemacht durch die[Anmerkung](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) -Klasse ermöglicht es Entwicklern, Kommentare auf der Zeichenseite Visio zu bearbeiten.
#### **Programmierbeispiel für Kommentar bearbeiten**

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

## **Fügen Sie in der Zeichnung Visio einen Kommentar auf Formebene hinzu**
[Aspose.Diagram for .NET](https://www.aspose.com/products/diagram/net)API ermöglicht Entwicklern das Hinzufügen von Kommentaren zur Form in einer Visio Zeichnung.
### **Einen Kommentar hinzufügen**
Eine überladene AddComment-Methode, verfügbar gemacht durch die[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page)Die Klasse übernimmt eine Shape-Klasseninstanz und eine Textzeichenfolge des Kommentars.
#### **Programmierbeispiel Kommentar hinzufügen**
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
