---
title: Formato Visio Pagine
type: docs
weight: 60
url: /it/net/format-visio-pages/
description: Questa sezione spiega come applicare gli stili a una pagina visio con Aspose.Diagram.
---
Aspose.Diagram for .NET API consente agli sviluppatori di formattare le pagine di un file Visio Diagram. L'applicazione dei fogli di stile è uno di questi metodi per formattare le pagine Visio.
## **Applica i fogli di stile alla pagina Visio**
Aspose.Diagram for .NET API consente di formattare una pagina Visio utilizzando i fogli di stile. È possibile definire un foglio di stile e aggiungerlo alla raccolta di fogli di stile del documento Visio. Il metodo ApplyStyle della classe Page consente di applicare il foglio di stile definito alla pagina, come illustrato nell'esempio di codice seguente.

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
