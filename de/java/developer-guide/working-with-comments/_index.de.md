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
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddPageLevelCommentInVisio.class);
// Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add comment
diagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@");

// Save diagram
diagram.save(dataDir + "AddPageLevelCommentInVisio_Out.vdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Bearbeiten Sie einen Kommentar auf Seitenebene im Visio Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API unterstützt das Ändern des Kommentars auf Seitenebene auf der Zeichenseite Visio, die durch ein Symbol in der oberen linken Ecke der Seite dargestellt werden.
### **Kommentar bearbeiten**
Die Comment-Eigenschaft, die von der Annotation-Klasse verfügbar gemacht wird, ermöglicht Entwicklern das Bearbeiten von Kommentaren auf dem Zeichenblatt Visio.
#### **Programmierbeispiel für Kommentar bearbeiten**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(EditPageLevelCommentInVisio.class);
// load Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get collection of the annotations
AnnotationCollection annotations = diagram.getPages().getPage("Page-1").getPageSheet().getAnnotations();

// iterate through the annotations
for (Annotation annotation : (Iterable<Annotation>) annotations) 
{
    String comment = annotation.getComment().getValue();
    comment += "Updation mark";
    annotation.getComment().setValue(comment);
}
// save Visio
diagram.save(dataDir + "EditPageLevelCommentInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
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
