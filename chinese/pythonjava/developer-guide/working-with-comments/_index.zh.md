---
title: 使用评论
type: docs
weight: 210
url: /zh/python-java/working-with-comments/
description: 本页介绍如何使用 Aspose.Diagram 库在 Visio 绘图的页面上添加注释。
---
## **在 Visio 添加页面级评论**
Aspose.Diagram for Python via Java API allows developers to add comment anywhere on a page of [Visio图纸](DrawingComment.vsdx).
### **添加评论**
Page 类公开的 addComment 方法允许您向绘图页添加注释。它采用 X 和 Y 坐标以及注释字符串。

Microsoft Visio users add comments to the entire page that are presented by an icon in the upper-left corner of the page. Developers can add page level comments in the Visio. Aspose.Diagram for Python via Java API additionally supports to alter the page level comment in the Visio.
#### **添加页面级评论编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Comments-AddPageLevelCommentInVisio.py" >}}
## **在 Visio Diagram 中编辑页面级评论**
Aspose.Diagram for Python via Java API has support of altering the page-level comment on [Visio图纸](DrawingComment.vsdx)由页面左上角的图标显示的页面。
### **编辑评论**
Comment 属性由 Annotation 类公开，允许开发人员在 Visio 绘图页中编辑注释。
#### **编辑评论编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Comments-EditPageLevelCommentInVisio.py" >}}
## **在 Visio 绘图中添加形状级注释**
Aspose.Diagram for Python via Java API allows developers to add comments to the shape in [Visio图纸](DrawingComment.vsdx).
### **添加评论**
Page 类公开的重载 addComment 方法采用 Shape 类实例和评论的文本字符串。
#### **添加形状级注释编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Comments-AddShapeLevelCommentInVisio.py" >}}
