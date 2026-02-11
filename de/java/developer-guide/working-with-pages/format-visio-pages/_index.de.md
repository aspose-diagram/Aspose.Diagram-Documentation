---
title: Format Visio Seiten
type: docs
weight: 40
url: /de/java/format-visio-pages/
---
Aspose.Diagram for Java API ermöglicht es Entwicklern, Seiten einer Visio Diagram-Datei zu formatieren. Das Anwenden von Stylesheets ist eine solche Methode zum Formatieren von Visio-Seiten.
## **Wenden Sie Stylesheets auf die Seite Visio an**
Mit Aspose.Diagram for Java API können Sie eine Visio-Seite mithilfe von Stylesheets formatieren. Sie können ein Stylesheet definieren und es der Stylesheet-Sammlung des Dokuments Visio hinzufügen. Mit der ApplyStyle-Methode der Page-Klasse können Sie das definierte Stylesheet auf die Seite anwenden, wie im folgenden Codebeispiel gezeigt.

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
