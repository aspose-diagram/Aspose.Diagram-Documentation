---
title: Format Visio Pages
type: docs
weight: 60
url: /net/format-visio-pages/
description: This section explains how to apply styles to a visio page with Aspose.Diagram.
---

Aspose.Diagram for .NET API allows developers to format pages of a Visio Diagram file. Applying Stylesheets is one such method to format Visio pages.
## **Apply Stylesheets to Visio Page**
Aspose.Diagram for .NET API lets you format a Visio page using Stylesheets. You can define a stylesheet and add it to the Visio document's stylesheet collection. The ApplyStyle method of Page class lets you apply the defined stylesheet to the page as shown in the following code sample.


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

