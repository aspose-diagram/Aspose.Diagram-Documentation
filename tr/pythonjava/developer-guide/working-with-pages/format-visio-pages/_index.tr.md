---
title: Biçim Visio Sayfa
type: docs
weight: 40
url: /tr/python-java/format-visio-pages/
---
Python via Java API için Aspose.Diagram, geliştiricilerin bir Visio Diagram dosyasının sayfalarını biçimlendirmesine olanak tanır. Stil Sayfalarını uygulamak, Visio sayfaları biçimlendirmek için böyle bir yöntemdir.

## **Stil Sayfalarını Visio Sayfasına Uygula**
Python için Aspose.Diagram via Java API, Stil Sayfalarını kullanarak bir Visio sayfasını biçimlendirmenizi sağlar. Bir stil sayfası tanımlayabilir ve bunu Visio belgesinin stil sayfası koleksiyonuna ekleyebilirsiniz. `Page` sınıfının `applyStyle` yöntemi, aşağıdaki kod örneğinde gösterildiği gibi, tanımlanan stil sayfasını sayfaya uygulamanıza izin verir.

```
{{< highlight "python" >}}
import jpype
import asposediagram

jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Open the stream. Read only access is enough for Aspose.Diagram to
# load a diagram.
stream = java.io.FileInputStream("ReadDiagramFile.vsd")

# load diagram
vsdDiagram = Diagram(stream)
# Define a new StyleSheet
st = StyleSheet()
st.setID(vsdDiagram.getStyleSheets().getCount() + 1)
ch = Char()
ch.getColor().setValue("#00ff00")
ch.setIX(0)
st.getChars().add(ch)

st.getLine().getLineColor().setValue("#ff0000")
st.getLine().getLinePattern().setValue(1)

st.getLine().getLineWeight().setValue(0.01)
st.getFill().getFillForegnd().setValue("#0000ff")
st.getFill().getFillPattern().setValue(1)
st.getFill().getShdwPattern().setValue(0)

# Add the stylesheet to Stylesheets collection
vsdDiagram.getStyleSheets().add(st)

for shape in vsdDiagram.getPages().get(0).getShapes():
    shape.getLine().getLinePattern().setValue(1)
    shape.getFill().getFillPattern().setValue(1)

# Apply the stylesheet
vsdDiagram.getPages().get(0).applyStyle(st.getID(), st.getID(), st.getID())

vsdDiagram.save("ApplyStyleToVisioDiagramPage_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
