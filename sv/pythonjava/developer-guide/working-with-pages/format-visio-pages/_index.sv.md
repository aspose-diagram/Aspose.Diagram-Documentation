---
title: Format Visio Sidor
type: docs
weight: 40
url: /sv/python-java/format-visio-pages/
---
Aspose.Diagram för Python via Java API tillåter utvecklare att formatera sidor i en Visio Diagram fil. Att använda formatmallar är en sådan metod för att formatera Visio sidor.

## **Applicera formatmallar på sidan Visio**
Aspose.Diagram för Python via Java API låter dig formatera en Visio sida med formatmallar. Du kan definiera en stilmall och lägga till den i Visio-dokumentets stilmallssamling. Metoden `applyStyle` i klassen `Page` låter dig tillämpa den definierade stilmallen på sidan som visas i följande kodexempel.


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

