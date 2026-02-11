---
title: Format Visio pages
type: docs
weight: 60
url: /fr/net/format-visio-pages/
description: Cette section explique comment appliquer des styles à une page visio avec Aspose.Diagram.
---
Aspose.Diagram for .NET API permet aux développeurs de formater les pages d'un fichier Visio Diagram. L'application de feuilles de style est l'une de ces méthodes pour formater les pages Visio.
## **Appliquer des feuilles de style à la page Visio**
Aspose.Diagram for .NET API vous permet de formater une page Visio à l'aide de feuilles de style. Vous pouvez définir une feuille de style et l'ajouter à la collection de feuilles de style du document Visio. La méthode ApplyStyle de la classe Page vous permet d'appliquer la feuille de style définie à la page, comme illustré dans l'exemple de code suivant.

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
