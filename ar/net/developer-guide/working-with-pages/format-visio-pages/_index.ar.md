---
title: تنسيق Visio صفحة
type: docs
weight: 60
url: /ar/net/format-visio-pages/
description: يشرح هذا القسم كيفية تطبيق الأنماط على صفحة visio باستخدام Aspose.Diagram.
---
Aspose.Diagram for .NET API يسمح للمطورين بتنسيق صفحات ملف Visio Diagram. يعد تطبيق Stylesheets أحد هذه الطرق لتنسيق Visio صفحات.
## **تطبيق أوراق الأنماط على Visio صفحة**
Aspose.Diagram for .NET API يتيح لك تنسيق صفحة Visio باستخدام Stylesheets. يمكنك تعريف ورقة أنماط وإضافتها إلى مجموعة ورقة أنماط الوثيقة Visio. تتيح لك طريقة ApplyStyle لفئة الصفحة تطبيق ورقة الأنماط المحددة على الصفحة كما هو موضح في نموذج التعليمات البرمجية التالي.

```
{{< highlight "csharp" >}}
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
```
