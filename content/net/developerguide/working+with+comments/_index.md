---
title : "Working with Comments" 
description : "" 
weight : 8054 
toc : false
type: docs
url: /net/developerguide/working+with+comments/
---

# Aspose.Diagram for .NET : Working with Comments


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Add a Page-Level Comment in the Visio](#add-a-page-level-comment-in-the-visio)
    *   1.1 [Add Comment](#add-comment)
        *   1.1.1 [Add Comment Programming Sample](#add-comment-programming-sample)
*   2 [Edit a Page-Level Comment in the Visio Diagram](#edit-a-page-level-comment-in-the-visio-diagram)
    *   2.1 [Edit Comment](#edit-comment)
        *   2.1.1 [Edit Comment Programming Sample](#edit-comment-programming-sample)
*   3 [Add a Shape-Level Comment in Visio Drawing](#add-a-shape-level-comment-in-visio-drawing)
    *   3.1 [Add Comment](#add-comment)
        *   3.1.1 [Add Comment Programming Sample](#add-comment-programming-sample)
{{< /panel >}}
 

 

## Add a Page-Level Comment in the Visio

[Aspose.Diagram for .NET](https://www.aspose.com/products/diagram/net) API allows developers to place comments anywhere in the Visio drawing page.

### Add Comment

The `AddComment` method, exposed by the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class, allows developers to add comments to a drawing page. It takes the X and Y coordinates along with a comment string.

#### Add Comment Programming Sample

## Edit a Page-Level Comment in the Visio Diagram

Microsoft Visio users add comments to the entire page that are presented by an icon in the upper-left corner of the page. Developers can [add page level comments in the Visio](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API additionally supports to alter the page level comment in the Visio.

### Edit Comment

The `Comment` property, exposed by the [Annotation](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) class, allows developers to edit comments in the Visio drawing page.

#### Edit Comment Programming Sample

## Add a Shape-Level Comment in Visio Drawing

[Aspose.Diagram for .NET](https://www.aspose.com/products/diagram/net) API allows developers to add comments to the shape in a Visio drawing.

### Add Comment

An overloaded `AddComment` method, exposed by the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class takes a Shape class instance and text string of the comment.

#### Add Comment Programming Sample

**C#**

{{< code lang="c#" >}}
// load diagram
Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");
// retrieve page by name
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");
// retrieve shape by ID
Aspose.Diagram.Shape shape = page.Shapes.GetShape(12);
page.AddComment(shape, "Hello");
// save diagram
diagram.Save(@"c:\temp\Drawing1.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

