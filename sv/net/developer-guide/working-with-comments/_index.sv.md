---
title: Arbeta med kommentarer
type: docs
weight: 220
url: /sv/net/working-with-comments/
description: Den här sidan beskriver hur man lägger till eller redigerar kommentarer med Aspose.Diagram-biblioteket.
---
## **Lägg till en kommentar på sidnivå i Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API tillåter utvecklare att lägga kommentarer var som helst på ritsidan Visio.
### **Lägg till kommentar**
 AddComment-metoden, exponerad av[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass, låter utvecklare lägga till kommentarer på en ritsida. Den tar X- och Y-koordinaterna tillsammans med en kommentarsträng.
#### **Lägg till kommentar Programmeringsexempel**
```
{{< highlight "csharp" >}}
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
```
## **Redigera en kommentar på sidnivå i Visio Diagram**
 Microsoft Visio användare lägger till kommentarer på hela sidan som presenteras av en ikon i det övre vänstra hörnet på sidan. Utvecklare kan[lägg till kommentarer på sidnivå i Visio](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API stöder dessutom att ändra sidnivåkommentaren i Visio.
### **Redigera kommentar**
 Egenskapen Kommentar, exponerad av[Anteckning](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) klass, tillåter utvecklare att redigera kommentarer på ritsidan Visio.
#### **Redigera kommentar Programmeringsexempel**
```
{{< highlight "csharp" >}}
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
```
## **Lägg till en kommentar på formnivå i Visio Ritning**
[Aspose.Diagram for .NET](https://www.aspose.com/products/diagram/net)API låter utvecklare lägga till kommentarer till formen i en Visio-ritning.
### **Lägg till kommentar**
En överbelastad AddComment-metod, exponerad av[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page)class tar en Shape-klassinstans och textsträng för kommentaren.
#### **Lägg till kommentar Programmeringsexempel**
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
