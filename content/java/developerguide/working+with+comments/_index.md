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

## Attachments:

![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Retrieve Visio shapes information-001.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809135.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Setting-XForm-data.003.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809134.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Setting-XForm-data-004.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809139.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Setting-Line-data-003.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809138.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Setting-Line-data-004.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809137.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Setting-Fill-data-001.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809136.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Setting-Fill-data-002.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809144.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Applying-custom-style-sheets-001.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809145.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Applying-custom-style-sheets-002.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809146.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Reading shape data-001.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809147.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Set-Height-and-Width-01.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809148.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Set-Height-and-Width-02.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809149.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Change the Position of a Shape-01.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809150.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Change the Position of a Shape-02.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809151.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Connect Sub-shapes of the Groups 001.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809152.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Connect Sub-shapes of the Groups 002.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809153.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Glue Visio Shapes Through the Connection Points-01.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809154.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Glue Visio Shapes Through the Connection Points-02.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809155.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Glue Group Shapes Inside the Container\_01.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809156.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Glue Group Shapes Inside the Container\_02.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809157.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Set Milestone Shape Properties 01.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809158.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Set Milestone Shape Properties 02.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809159.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Set Time Period and Date Format of TimeLine Shape 01.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809141.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Set Time Period and Date Format of TimeLine Shape 02.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809140.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Set Time Period and Date Format of TimeLine Shape 03.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809143.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Set Time Period and Date Format of TimeLine Shape 04.png](https://docs2.aspose.com/diagram/java/attachments/18612508/18809142.png) (image/png)  

