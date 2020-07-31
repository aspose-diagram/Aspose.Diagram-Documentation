---
title : "Working with Comments" 
description : "" 
weight : 8054 
toc : false
type: docs
url: /java/developerguide/working+with+comments/
---

# Aspose.Diagram for Java : Working with Comments


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

Aspose.Diagram for Java API allows developers to add comment anywhere on a page of the Visio drawing.

### Add Comment

The `addComment` method, exposed by the `Page` class, allows you to add comments to a drawing page. It takes the X and Y coordinates along with a comment string.

Microsoft Visio users add comments to the entire page that are presented by an icon in the upper-left corner of the page. Developers can [add page level comments in the Visio](#). [Aspose.Diagram for Java](http://www.aspose.com/java/diagram-component.aspx) API additionally supports to alter the page level comment in the Visio.

#### Add Comment Programming Sample

## Edit a Page-Level Comment in the Visio Diagram

 [Aspose.Diagram for Java](https://www.aspose.com/products/diagram/java) API has support of altering the page-level comment on the Visio drawing page which are presented by an icon in the upper-left corner of the page. 

### Edit Comment

The `Comment` property, exposed by the `Annotation` class, allows developers to edit comments in the Visio drawing page.

#### Edit Comment Programming Sample

## Add a Shape-Level Comment in Visio Drawing

[Aspose.Diagram for Java](https://www.aspose.com/products/diagram/java) API allows developers to add comments to the shape in a Visio drawing.

### Add Comment

An overloaded a`ddComment` method, exposed by the Page class takes a Shape class instance and text string of the comment.

#### Add Comment Programming Sample

**Java**

{{< code lang="java" >}}
// load diagram
Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");
// retrieve page by name
Page page = diagram.getPages().getPage("Page-1");
// retrieve shape by ID
Shape shape = page.getShapes().getShape(12);
page.addComment(shape, "Hello");
// save diagram
diagram.save("c:\\temp\\Drawing1.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

