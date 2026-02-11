---
title: Biçim Visio Sayfa
type: docs
weight: 40
url: /tr/java/format-visio-pages/
---
Aspose.Diagram for Java API, geliştiricilerin bir Visio Diagram dosyasının sayfalarını biçimlendirmesine olanak tanır. Stil Sayfalarını uygulamak, Visio sayfaları biçimlendirmek için böyle bir yöntemdir.
## **Stil Sayfalarını Visio Sayfasına Uygula**
Aspose.Diagram for Java API, Stil Sayfalarını kullanarak bir Visio sayfasını biçimlendirmenizi sağlar. Bir stil sayfası tanımlayabilir ve bunu Visio belgesinin stil sayfası koleksiyonuna ekleyebilirsiniz. Page sınıfının ApplyStyle yöntemi, aşağıdaki kod örneğinde gösterildiği gibi, tanımlanan stil sayfasını sayfaya uygulamanıza izin verir.


{{< highlight java >}}
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

