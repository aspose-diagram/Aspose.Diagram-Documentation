---
title: تنسيق Visio صفحة
type: docs
weight: 40
url: /ar/python-java/format-visio-pages/
---
Aspose.Diagram لـ Python via Java API يسمح للمطورين بتنسيق صفحات ملف Visio Diagram. يعد تطبيق Stylesheets أحد هذه الطرق لتنسيق Visio صفحات.

## **تطبيق أوراق الأنماط على Visio صفحة**
Aspose.Diagram لـ Python via Java API يتيح لك تنسيق صفحة Visio باستخدام Stylesheets. يمكنك تعريف ورقة أنماط وإضافتها إلى مجموعة ورقة أنماط الوثيقة Visio. تتيح لك طريقة `applyStyle` لفئة `Page` تطبيق ورقة الأنماط المحددة على الصفحة كما هو موضح في نموذج التعليمات البرمجية التالي.


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

