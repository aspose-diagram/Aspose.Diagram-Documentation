---
title: Biçim Visio Sayfa
type: docs
weight: 60
url: /tr/net/format-visio-pages/
description: Bu bölümde, Aspose.Diagram ile visio sayfasına stillerin nasıl uygulanacağı açıklanmaktadır.
---
Aspose.Diagram for .NET API, geliştiricilerin bir Visio Diagram dosyasının sayfalarını biçimlendirmesine olanak tanır. Stil Sayfalarını uygulamak, Visio sayfaları biçimlendirmek için böyle bir yöntemdir.
## **Stil Sayfalarını Visio Sayfasına Uygula**
Aspose.Diagram for .NET API, Stil Sayfalarını kullanarak bir Visio sayfasını biçimlendirmenizi sağlar. Bir stil sayfası tanımlayabilir ve bunu Visio belgesinin stil sayfası koleksiyonuna ekleyebilirsiniz. Page sınıfının ApplyStyle yöntemi, aşağıdaki kod örneğinde gösterildiği gibi, tanımlanan stil sayfasını sayfaya uygulamanıza izin verir.

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
