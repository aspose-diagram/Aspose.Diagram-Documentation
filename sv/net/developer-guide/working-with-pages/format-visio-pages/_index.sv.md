---
title: Format Visio Sidor
type: docs
weight: 60
url: /sv/net/format-visio-pages/
description: Det här avsnittet förklarar hur du tillämpar stilar på en visio-sida med Aspose.Diagram.
---
Aspose.Diagram for .NET API tillåter utvecklare att formatera sidor i en Visio Diagram fil. Att använda formatmallar är en sådan metod för att formatera Visio sidor.
## **Applicera formatmallar på sidan Visio**
Aspose.Diagram for .NET API låter dig formatera en Visio sida med formatmallar. Du kan definiera en stilmall och lägga till den i Visio-dokumentets stilmallssamling. ApplyStyle-metoden för klassen Page låter dig tillämpa den definierade stilmallen på sidan som visas i följande kodexempel.

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
