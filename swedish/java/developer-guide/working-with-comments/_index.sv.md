---
title: Arbeta med kommentarer
type: docs
weight: 210
url: /sv/java/working-with-comments/
---
## **Lägg till en kommentar på sidnivå i Visio**
Aspose.Diagram for Java API tillåter utvecklare att lägga till kommentarer var som helst på en sida i Visio-ritningen.
### **Lägg till kommentar**
Metoden addComment, exponerad av klassen Page, låter dig lägga till kommentarer på en ritsida. Den tar X- och Y-koordinaterna tillsammans med en kommentarsträng.

 Microsoft Visio användare lägger till kommentarer på hela sidan som presenteras av en ikon i det övre vänstra hörnet på sidan. Utvecklare kan[lägg till kommentarer på sidnivå i Visio](). [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API stöder dessutom att ändra sidnivåkommentaren i Visio.
#### **Lägg till kommentar Programmeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.java" >}}
## **Redigera en kommentar på sidnivå i Visio Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API har stöd för att ändra sidnivåkommentaren på Visio ritsidan som presenteras av en ikon i det övre vänstra hörnet på sidan.
### **Redigera kommentar**
Egenskapen Comment, exponerad av klassen Annotation, tillåter utvecklare att redigera kommentarer på ritsidan Visio.
#### **Redigera kommentar Programmeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.java" >}}
## **Lägg till en kommentar på formnivå i Visio Ritning**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API låter utvecklare lägga till kommentarer till formen i en Visio-ritning.
### **Lägg till kommentar**
En överbelastad addComment-metod, som exponeras av klassen Page, tar en Shape-klassinstans och textsträng av kommentaren.
#### **Lägg till kommentar Programmeringsexempel**
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
