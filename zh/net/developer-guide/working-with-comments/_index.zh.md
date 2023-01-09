---
title: 使用评论
type: docs
weight: 220
url: /zh/net/working-with-comments/
description: 本页介绍如何使用 Aspose.Diagram 库添加或编辑评论。
---
## **在 Visio 添加页面级评论**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API 允许开发人员在 Visio 绘图页的任何位置放置注释。
### **添加评论**
 AddComment 方法，由[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)类，允许开发人员向绘图页添加注释。它采用 X 和 Y 坐标以及注释字符串。
#### **添加评论编程示例**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.cs" >}}
## **在 Visio Diagram 中编辑页面级评论**
 Microsoft Visio 用户向整个页面添加评论，通过页面左上角的图标显示。开发者可以[在 Visio 添加页面级评论](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API 还支持修改 Visio 中的页面级注释。
### **编辑评论**
 Comment 属性，由[注解](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation)类，允许开发人员在 Visio 绘图页中编辑注释。
#### **编辑评论编程示例**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.cs" >}}
## **在 Visio 绘图中添加形状级注释**
[Aspose.Diagram for .NET](https://www.aspose.com/products/diagram/net)API 允许开发人员向 Visio 绘图中的形状添加注释。
### **添加评论**
重载的 AddComment 方法，由[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)类采用 Shape 类实例和评论的文本字符串。
#### **添加评论编程示例**
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
