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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.cs" >}}
## **Bearbeiten Sie einen Kommentar auf Seitenebene im Visio Diagram**
 Microsoft Visio Benutzer fügen der gesamten Seite Kommentare hinzu, die durch ein Symbol in der oberen linken Ecke der Seite angezeigt werden. Entwickler können[Kommentare auf Seitenebene in Visio hinzufügen](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API unterstützt zusätzlich das Ändern des Kommentars auf Seitenebene in Visio.
### **Kommentar bearbeiten**
 Die Comment-Eigenschaft, verfügbar gemacht durch die[Anmerkung](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) -Klasse ermöglicht es Entwicklern, Kommentare auf der Zeichenseite Visio zu bearbeiten.
#### **Programmierbeispiel für Kommentar bearbeiten**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.cs" >}}
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
