---
title: 使用评论
type: docs
weight: 210
url: /zh/java/working-with-comments/
---
## **在 Visio 添加页面级评论**
Aspose.Diagram for Java API 允许开发人员在 Visio 图的页面上的任何位置添加注释。
### **添加评论**
Page 类公开的 addComment 方法允许您向绘图页添加注释。它采用 X 和 Y 坐标以及注释字符串。

 Microsoft Visio 用户向整个页面添加评论，通过页面左上角的图标显示。开发者可以[在 Visio 添加页面级评论](). [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API 还支持修改 Visio 中的页面级注释。
#### **添加评论编程示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.java" >}}
## **在 Visio Diagram 中编辑页面级评论**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API支持修改Visio绘图页的页面级注释，在页面左上角以图标显示。
### **编辑评论**
Comment 属性由 Annotation 类公开，允许开发人员在 Visio 绘图页中编辑注释。
#### **编辑评论编程示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.java" >}}
## **在 Visio 绘图中添加形状级注释**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API 允许开发人员向 Visio 绘图中的形状添加注释。
### **添加评论**
Page 类公开的重载 addComment 方法采用 Shape 类实例和评论的文本字符串。
#### **添加评论编程示例**
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
