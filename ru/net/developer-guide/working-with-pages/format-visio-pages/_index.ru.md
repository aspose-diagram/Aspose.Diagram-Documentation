---
title: Формат Visio Страницы
type: docs
weight: 60
url: /ru/net/format-visio-pages/
description: В этом разделе объясняется, как применять стили к странице visio с Aspose.Diagram.
---
Aspose.Diagram for .NET API позволяет разработчикам форматировать страницы файла Visio Diagram. Применение таблиц стилей — один из таких способов форматирования Visio страниц.
## **Применить таблицы стилей к странице Visio**
Aspose.Diagram for .NET API позволяет форматировать страницу Visio с помощью таблиц стилей. Вы можете определить таблицу стилей и добавить ее в коллекцию таблиц стилей документа Visio. Метод ApplyStyle класса Page позволяет применить определенную таблицу стилей к странице, как показано в следующем примере кода.

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
