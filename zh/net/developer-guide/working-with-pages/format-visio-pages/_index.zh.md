---
title: 格式 Visio 页
type: docs
weight: 60
url: /zh/net/format-visio-pages/
description: 本节介绍如何将样式应用于带有 Aspose.Diagram 的 visio 页面。
---
Aspose.Diagram for .NET API 允许开发人员格式化 Visio Diagram 文件的页面。应用样式表就是这样一种格式化 Visio 页面的方法。
## **将样式表应用于 Visio 页面**
Aspose.Diagram for .NET API 允许您使用样式表格式化 Visio 页面。您可以定义样式表并将其添加到 Visio 文档的样式表集合中。 Page 类的 ApplyStyle 方法允许您将定义的样式表应用到页面，如以下代码示例所示。


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD stream
FileStream stream = new FileStream(dataDir + "ReadDiagramFile.vsd", FileMode.Open);
// Load diagram
Diagram vsdDiagram = new Diagram(stream);

//Define a new StyleSheet
StyleSheet st = new StyleSheet();
st.ID = vsdDiagram.StyleSheets.Count + 1;
Aspose.Diagram.Char ch = new Aspose.Diagram.Char();
ch.Color.Value = "#00ff00";
ch.IX = 0;
st.Chars.Add(ch);
st.Line.LineColor.Value = "#ff0000";
st.Line.LinePattern.Value = 1;
st.Line.LineWeight.Value = 0.01;
st.Fill.FillForegnd.Value = "#0000ff";
st.Fill.FillPattern.Value = 1;
st.Fill.ShdwPattern.Value = 0;

//Add the stylesheet to Stylesheets collection
vsdDiagram.StyleSheets.Add(st);

foreach (Shape shape in vsdDiagram.Pages[0].Shapes)
{
    shape.Line.LinePattern.Value = 1;
    shape.Fill.FillPattern.Value = 1;
}

//Apply the stylesheet
vsdDiagram.Pages[0].ApplyStyle(st.ID, st.ID, st.ID);

{{< /highlight >}}

