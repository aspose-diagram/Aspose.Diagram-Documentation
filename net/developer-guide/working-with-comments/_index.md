---
title: Working with Comments
type: docs
weight: 220
url: /net/working-with-comments/
---

## **Add a Page-Level Comment in the Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net) API allows developers to place comments anywhere in the Visio drawing page.
### **Add Comment**
The AddComment method, exposed by the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class, allows developers to add comments to a drawing page. It takes the X and Y coordinates along with a comment string.
#### **Add Comment Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.cs" >}}
## **Edit a Page-Level Comment in the Visio Diagram**
Microsoft Visio users add comments to the entire page that are presented by an icon in the upper-left corner of the page. Developers can [add page level comments in the Visio](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net) API additionally supports to alter the page level comment in the Visio.
### **Edit Comment**
The Comment property, exposed by the [Annotation](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) class, allows developers to edit comments in the Visio drawing page.
#### **Edit Comment Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.cs" >}}
## **Add a Shape-Level Comment in Visio Drawing**
[Aspose.Diagram for .NET](https://www.aspose.com/products/diagram/net) API allows developers to add comments to the shape in a Visio drawing.
### **Add Comment**
An overloaded AddComment method, exposed by the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class takes a Shape class instance and text string of the comment.
#### **Add Comment Programming Sample**
**C#**

{{< highlight java >}}

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
