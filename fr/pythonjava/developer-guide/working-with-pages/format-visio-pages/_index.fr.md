---
title: Format Visio pages
type: docs
weight: 40
url: /fr/python-java/format-visio-pages/
---
Aspose.Diagram for Python via Java API allows developers to format pages of a Visio Diagram file. Applying Stylesheets is one such method to format Visio pages.

## **Appliquer des feuilles de style à la page Visio**
Aspose.Diagram for Python via Java API lets you format a Visio page using Stylesheets. You can define a stylesheet and add it to the Visio document's stylesheet collection. The `applyStyle` method of `Page` class lets you apply the defined stylesheet to the page as shown in the following code sample.


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

