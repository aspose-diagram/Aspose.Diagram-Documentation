---
title: Working with Comments
type: docs
weight: 210
url: /java/working-with-comments/
---

## **Add a Page-Level Comment in the Visio**
Aspose.Diagram for Java API allows developers to add comment anywhere on a page of the Visio drawing.
### **Add Comment**
The addComment method, exposed by the Page class, allows you to add comments to a drawing page. It takes the X and Y coordinates along with a comment string.

Microsoft Visio users add comments to the entire page that are presented by an icon in the upper-left corner of the page. Developers can [add page level comments in the Visio](). [Aspose.Diagram for Java](https://products.aspose.com/diagram/java) API additionally supports to alter the page level comment in the Visio.
#### **Add Comment Programming Sample**
{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.java" >}}
## **Edit a Page-Level Comment in the Visio Diagram**
` `[Aspose.Diagram for Java](https://products.aspose.com/diagram/java) API has support of altering the page-level comment on the Visio drawing page which are presented by an icon in the upper-left corner of the page. 
### **Edit Comment**
The Comment property, exposed by the Annotation class, allows developers to edit comments in the Visio drawing page.
#### **Edit Comment Programming Sample**
{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.java" >}}
## **Add a Shape-Level Comment in Visio Drawing**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java) API allows developers to add comments to the shape in a Visio drawing.
### **Add Comment**
An overloaded addComment method, exposed by the Page class takes a Shape class instance and text string of the comment.
#### **Add Comment Programming Sample**
**Java**

{{< highlight java >}}

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
