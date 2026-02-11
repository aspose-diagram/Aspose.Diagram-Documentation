---
title: 格式 Visio 页
type: docs
weight: 40
url: /zh/java/format-visio-pages/
---
Aspose.Diagram for Java API 允许开发人员格式化 Visio Diagram 文件的页面。应用样式表就是这样一种格式化 Visio 页面的方法。
## **将样式表应用于 Visio 页面**
Aspose.Diagram for Java API 允许您使用样式表格式化 Visio 页面。您可以定义样式表并将其添加到 Visio 文档的样式表集合中。 Page 类的 ApplyStyle 方法允许您将定义的样式表应用到页面，如以下代码示例所示。

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ReadDiagramFile.class) + "Diagrams/";
// Open the stream. Read only access is enough for Aspose.Diagram to
// load a diagram.
InputStream stream = new FileInputStream(dataDir + "ReadDiagramFile.vsd");

// load diagram
Diagram vsdDiagram = new Diagram(stream);
//Define a new StyleSheet
StyleSheet st = new StyleSheet();
st.setID(vsdDiagram.getStyleSheets().getCount()+1);
com.aspose.diagram.Char ch = new com.aspose.diagram.Char();
ch.getColor().setValue("#00ff00");
ch.setIX(0);
st.getChars().add(ch);
		
st.getLine().getLineColor().setValue("#ff0000");
st.getLine().getLinePattern().setValue(1);
		
st.getLine().getLineWeight().setValue(0.01);
st.getFill().getFillForegnd().setValue("#0000ff");
st.getFill().getFillPattern().setValue(1);
st.getFill().getShdwPattern().setValue(0);

//Add the stylesheet to Stylesheets collection
vsdDiagram.getStyleSheets().add(st);

for (Shape shape: (Iterable<Shape>)vsdDiagram.getPages().get(0).getShapes())
{
    shape.getLine().getLinePattern().setValue(1);
    shape.getFill().getFillPattern().setValue(1);
}

//Apply the stylesheet
vsdDiagram.getPages().get(0).applyStyle(st.getID(), st.getID(), st.getID());

{{< /highlight >}}
```
