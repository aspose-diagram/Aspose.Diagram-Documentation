---
title: 使用评论
type: docs
weight: 210
url: /zh/python-java/working-with-comments/
description: 本页介绍如何使用 Aspose.Diagram 库在 Visio 绘图的页面上添加注释。
---
## **在 Visio 添加页面级评论**
 Aspose.Diagram for Python via Java API 允许开发人员在页面的任何位置添加评论[Visio图纸](DrawingComment.vsdx).
### **添加评论**
Page 类公开的 addComment 方法允许您向绘图页添加注释。它采用 X 和 Y 坐标以及注释字符串。

Microsoft Visio 用户向整个页面添加评论，通过页面左上角的图标显示。开发者可以在Visio添加页面级注释。Aspose.Diagram为Python通过Java API另外支持修改Visio中的页面级注释。
#### **添加页面级评论编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Comments-AddPageLevelCommentInVisio.py" >}}
## **在 Visio Diagram 中编辑页面级评论**
Aspose.Diagram for Python via Java API 支持修改页面级评论[Visio图纸](DrawingComment.vsdx)由页面左上角的图标显示的页面。
### **编辑评论**
Comment 属性由 Annotation 类公开，允许开发人员在 Visio 绘图页中编辑注释。
#### **编辑评论编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Comments-EditPageLevelCommentInVisio.py" >}}
## **在 Visio 绘图中添加形状级注释**
Aspose.Diagram for Python via Java API 允许开发人员在形状中添加注释[Visio图纸](DrawingComment.vsdx).
### **添加评论**
Page 类公开的重载 addComment 方法采用 Shape 类实例和评论的文本字符串。
#### **添加形状级注释编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Comments-AddShapeLevelCommentInVisio.py" >}}
