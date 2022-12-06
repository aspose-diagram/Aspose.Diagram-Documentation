---
title: Arbeiten mit Kommentaren
type: docs
weight: 210
url: /de/java/working-with-comments/
---
## **Fügen Sie einen Kommentar auf Seitenebene in Visio hinzu**
Aspose.Diagram for Java API ermöglicht Entwicklern das Hinzufügen von Kommentaren überall auf einer Seite der Zeichnung Visio.
### **Einen Kommentar hinzufügen**
Die addComment-Methode, die von der Page-Klasse bereitgestellt wird, ermöglicht das Hinzufügen von Kommentaren zu einem Zeichenblatt. Es nimmt die X- und Y-Koordinaten zusammen mit einer Kommentarzeichenfolge.

 Microsoft Visio Benutzer fügen der gesamten Seite Kommentare hinzu, die durch ein Symbol in der oberen linken Ecke der Seite angezeigt werden. Entwickler können[Kommentare auf Seitenebene in Visio hinzufügen](). [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API unterstützt zusätzlich das Ändern des Kommentars auf Seitenebene in Visio.
#### **Programmierbeispiel Kommentar hinzufügen**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.java" >}}
## **Bearbeiten Sie einen Kommentar auf Seitenebene im Visio Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API unterstützt das Ändern des Kommentars auf Seitenebene auf der Zeichenseite Visio, die durch ein Symbol in der oberen linken Ecke der Seite dargestellt werden.
### **Kommentar bearbeiten**
Die Comment-Eigenschaft, die von der Annotation-Klasse verfügbar gemacht wird, ermöglicht Entwicklern das Bearbeiten von Kommentaren auf dem Zeichenblatt Visio.
#### **Programmierbeispiel für Kommentar bearbeiten**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.java" >}}
## **Fügen Sie in der Zeichnung Visio einen Kommentar auf Formebene hinzu**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API ermöglicht Entwicklern das Hinzufügen von Kommentaren zur Form in einer Visio Zeichnung.
### **Einen Kommentar hinzufügen**
Eine überladene addComment-Methode, die von der Page-Klasse verfügbar gemacht wird, übernimmt eine Shape-Klasseninstanz und eine Textzeichenfolge des Kommentars.
#### **Programmierbeispiel Kommentar hinzufügen**
**Java**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// retrieve page by name

Page page = diagram.getPages().getPage("Page-1");

// retrieve shape by ID

Shape shape = page.getShapes().getShape(12);

page.addComment(shape, "Hello");

// save diagram

diagram.save("c:\\temp\\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
