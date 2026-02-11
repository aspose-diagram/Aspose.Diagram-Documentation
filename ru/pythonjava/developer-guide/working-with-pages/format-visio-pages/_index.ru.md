---
title: Формат Visio Страницы
type: docs
weight: 40
url: /ru/python-java/format-visio-pages/
---
Aspose.Diagram для Python via Java API позволяет разработчикам форматировать страницы файла Visio Diagram. Применение таблиц стилей — один из таких способов форматирования Visio страниц.

## **Применить таблицы стилей к странице Visio**
Aspose.Diagram для Python via Java API позволяет форматировать страницу Visio с помощью таблиц стилей. Вы можете определить таблицу стилей и добавить ее в коллекцию таблиц стилей документа Visio. Метод `applyStyle` класса `Page` позволяет применить определенную таблицу стилей к странице, как показано в следующем примере кода.


{{< highlight python >}}
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

