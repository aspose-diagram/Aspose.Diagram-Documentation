---
title: العمل مع الطبقات
type: docs
weight: 160
url: /ar/python-java/working-with-layers/
---
### **تكوين كائنات الشكل مع الطبقات**
يسمح Aspose.Diagram لـ Python via Java بتكوين كائنات الشكل بطبقات في Microsoft Office Visio diagram يمكن أن ينتمي كل شكل إلى طبقات متعددة حتى يتمكن المطورون من إدارة الأشكال لتناسب احتياجات المستخدم النهائي.

 ال[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) يقدم كائن الفئة خاصية LayerMember التي تسمح بإضافة / إزالة كائنات الشكل من / إلى الطبقات في رسم Visio. يمكن للمستخدمين إدارة هذه الخصائص برمجيًا باستخدام Aspose.Diagram API على النحو التالي:

**قم بإضافة وإزالة وتحريك كائنات الشكل من / إلى طبقات diagram.** 

يساعد الجزء التالي من التعليمات البرمجية على إضافة خصائص كائنات الشكل وإزالتها ونقلها.
#### **عينات البرمجة**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")
        
# call the diagram constructor to load visio diagram
diagram = Diagram("DrawingFlowChart.vsdx")
        
# iterate through the shapes
for shape in diagram.getPages().getPage("Page-1").getShapes():
    if shape.getName().toLowerCase() == "shape1":
        # Add shape1 in first two layers. Here "0;1" are indexes of the layers
        layer = shape.getLayerMem()
        layer.getLayerMember().setValue("0;1")
    elif shape.getName().toLowerCase() == "shape2":
        # Remove shape2 from all the layers
        layer = shape.getLayerMem()
        layer.getLayerMember().setValue("")
    elif shape.getName().toLowerCase() == "shape3":
        # Add shape3 in first layer. Here "0" is index of the first layer
        layer = shape.getLayerMem()
        layer.getLayerMember().setValue("0")

# save diagram
diagram.save("ConfigureShapeLayers_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
### **أضف طبقة في Visio PageSheet**
Aspose.Diagram لـ Python via Java يسمح للمطورين بإضافة طبقات جديدة لتنظيم فئات مخصصة من الأشكال ، ثم تخصيص أشكال لتلك الطبقات برمجيًا.

 ال[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) يقدم class طريقة إضافة تسمح بإضافة ملف[طبقة](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) كائن فئة في[الرسم Visio](DrawingFlowChart.vsdx). يمكن للمطورين تعيين خصائص الطبقة عن طريق تهيئة كائن الفئة الخاص بها.

يساعد الجزء التالي من التعليمات البرمجية على إضافة كائنات الطبقة.
#### **عينات البرمجة**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load a source Visio diagram
diagram = Diagram("DrawingFlowChart.vsdx")
# get Visio page
page = diagram.getPages().getPage("Page-1")

# initialize a new Layer class object
layer = Layer()
# set Layer name
layer.getName().setValue("Layer1")
# set Layer Visibility
layer.getVisible().setValue(BOOL.TRUE)
# set the color checkbox of Layer
layer.setColorChecked(BOOL.TRUE)
# add Layer to the particular page sheet
page.getPageSheet().getLayers().add(layer)

# get shape by ID
shape = page.getShapes().getShape(3)
# assign shape to this new Layer
shape.getLayerMem().getLayerMember().setValue(str(layer.getIX()))
# save diagram
diagram.save("AddLayer_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```

{{% alert color="primary" %}} 

Aspose.Diagram لـ Python via Java يمنح المطورين الوصول إلى الطبقات الموجودة Visio diagram.

{{% /alert %}} 
### **احصل على جميع الطبقات المتاحة**
 ال[ورقة الصفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) ممتلكات[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) تسمح class باسترداد قائمة الطبقات المتاحة من[الرسم Visio](DrawingFlowChart.vsdx) استخدام[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) صف دراسي.

يساعد الجزء التالي من التعليمات البرمجية في الحصول على قائمة الطبقات.
#### **عينات البرمجة**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load Visio diagram
diagram = Diagram("DrawingFlowChart.vsdx")
# get Visio page
page = diagram.getPages().getPage("Page-1")

# iterate through the layers
for layer in page.getPageSheet().getLayers():
    print("Name: " + str(layer.getName().getValue()))
    print("Visibility: " + str(layer.getVisible().getValue()))
    print("Status: " + str(layer.getStatus().getValue()))

jpype.shutdownJVM()

{{< /highlight >}}
```
