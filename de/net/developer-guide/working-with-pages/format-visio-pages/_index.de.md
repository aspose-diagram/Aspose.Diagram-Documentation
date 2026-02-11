---
title: Format Visio Seiten
type: docs
weight: 60
url: /de/net/format-visio-pages/
description: In diesem Abschnitt wird erläutert, wie Sie Stile auf eine visio-Seite mit Aspose.Diagram anwenden.
---
Aspose.Diagram for .NET API ermöglicht es Entwicklern, Seiten einer Visio Diagram-Datei zu formatieren. Das Anwenden von Stylesheets ist eine solche Methode zum Formatieren von Visio-Seiten.
## **Wenden Sie Stylesheets auf die Seite Visio an**
Mit Aspose.Diagram for .NET API können Sie eine Visio-Seite mithilfe von Stylesheets formatieren. Sie können ein Stylesheet definieren und es der Stylesheet-Sammlung des Dokuments Visio hinzufügen. Mit der ApplyStyle-Methode der Page-Klasse können Sie das definierte Stylesheet auf die Seite anwenden, wie im folgenden Codebeispiel gezeigt.


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

