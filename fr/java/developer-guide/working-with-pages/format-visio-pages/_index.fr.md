---
title: Format Visio pages
type: docs
weight: 40
url: /fr/java/format-visio-pages/
---
Aspose.Diagram for Java API permet aux développeurs de formater les pages d'un fichier Visio Diagram. L'application de feuilles de style est l'une de ces méthodes pour formater les pages Visio.
## **Appliquer des feuilles de style à la page Visio**
Aspose.Diagram for Java API vous permet de formater une page Visio à l'aide de feuilles de style. Vous pouvez définir une feuille de style et l'ajouter à la collection de feuilles de style du document Visio. La méthode ApplyStyle de la classe Page vous permet d'appliquer la feuille de style définie à la page, comme illustré dans l'exemple de code suivant.

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
