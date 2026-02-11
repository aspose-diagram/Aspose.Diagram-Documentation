---
title: Formato Visio Páginas
type: docs
weight: 60
url: /es/net/format-visio-pages/
description: Esta sección explica cómo aplicar estilos a una página visio con Aspose.Diagram.
---
Aspose.Diagram for .NET API permite a los desarrolladores formatear páginas de un archivo Visio Diagram. La aplicación de hojas de estilo es uno de esos métodos para formatear Visio páginas.
## **Aplicar hojas de estilo a la página Visio**
Aspose.Diagram for .NET API le permite formatear una página Visio usando hojas de estilo. Puede definir una hoja de estilo y agregarla a la colección de hojas de estilo del documento Visio. El método ApplyStyle de la clase Page le permite aplicar la hoja de estilo definida a la página como se muestra en el siguiente ejemplo de código.

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
