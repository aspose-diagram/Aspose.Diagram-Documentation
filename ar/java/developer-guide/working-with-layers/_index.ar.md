---
title: العمل مع الطبقات
type: docs
weight: 160
url: /ar/java/working-with-layers/
---
### **تكوين كائنات الشكل مع الطبقات**
Aspose.Diagram for Java يسمح بتكوين كائنات الشكل بطبقات في Microsoft Office Visio diagram يمكن أن ينتمي كل شكل إلى طبقات متعددة بحيث يمكن للمطورين إدارة الأشكال لتناسب احتياجات المستخدم النهائي.

 ال[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) يقدم كائن الفئة خاصية LayerMember التي تسمح بإضافة / إزالة كائنات الشكل من / إلى الطبقات في رسم Visio. يمكن للمستخدمين إدارة هذه الخصائص برمجيًا باستخدام Aspose.Diagram API على النحو التالي:

**قم بإضافة وإزالة وتحريك كائنات الشكل من / إلى طبقات diagram.** 

![ما يجب القيام به: image_بديل_نص](working-with-layers_1.png)

يساعد الجزء التالي من التعليمات البرمجية على إضافة خصائص كائنات الشكل وإزالتها ونقلها.
#### **عينات البرمجة**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConfigureShapeLayers.class);
        
//call the diagram constructor to load visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
        
// iterate through the shapes
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage("Page-1").getShapes())
{
    if (shape.getName().toLowerCase() == "shape1")
    {
        //Add shape1 in first two layers. Here "0;1" are indexes of the layers
        LayerMem layer = shape.getLayerMem();
        layer.getLayerMember().setValue("0;1");
    }
    else if (shape.getName().toLowerCase() == "shape2")
    {
        //Remove shape2 from all the layers
        LayerMem layer = shape.getLayerMem();
        layer.getLayerMember().setValue("");
    }
    else if (shape.getName().toLowerCase() == "shape3")
    {
        //Add shape3 in first layer. Here "0" is index of the first layer
        LayerMem layer = shape.getLayerMem();
        layer.getLayerMember().setValue("0");
    }
}
// save diagram
diagram.save(dataDir + "ConfigureShapeLayers_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

### **أضف طبقة في Visio PageSheet**
Aspose.Diagram for Java يسمح للمطورين بإضافة طبقات جديدة لتنظيم الفئات المهيأة من الأشكال ، ثم تخصيص الأشكال لتلك الطبقات برمجيًا.

 ال[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) يقدم class طريقة إضافة تسمح بإضافة ملف[طبقة](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)كائن فئة في الرسم Visio. يمكن للمطورين تعيين خصائص الطبقة عن طريق تهيئة كائن الفئة الخاص بها.

يساعد الجزء التالي من التعليمات البرمجية على إضافة كائنات الطبقة.
#### **عينات البرمجة**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddLayer.class) + "Layers/";

// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page page = diagram.getPages().getPage("Page-1");

// initialize a new Layer class object
Layer layer = new Layer();
// set Layer name
layer.getName().setValue("Layer1");
// set Layer Visibility
layer.getVisible().setValue(BOOL.TRUE);
// set the color checkbox of Layer
layer.setColorChecked(BOOL.TRUE);
// add Layer to the particular page sheet
page.getPageSheet().getLayers().add(layer);

// get shape by ID
Shape shape = page.getShapes().getShape(3);
// assign shape to this new Layer
shape.getLayerMem().getLayerMember().setValue(Integer.toString(layer.getIX()));
// save diagram
diagram.save(dataDir + "AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}} 

Aspose.Diagram for Java يمنح المطورين الوصول إلى الطبقات الموجودة Visio diagram.

{{% /alert %}} 
### **احصل على جميع الطبقات المتاحة**
 ال[ورقة الصفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) ممتلكات[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) تسمح الفئة باسترداد قائمة الطبقات المتاحة من Visio diagram باستخدام[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) صف دراسي.

يساعد الجزء التالي من التعليمات البرمجية في الحصول على قائمة الطبقات.
#### **عينات البرمجة**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveAllLayers.class);  
// load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page page = diagram.getPages().getPage("Page-1");

// iterate through the layers
for (Layer layer : (Iterable<Layer>) page.getPageSheet().getLayers())
{
    System.out.println("Name: " + layer.getName().getValue());
    System.out.println("Visibility: " + layer.getVisible().getValue());
    System.out.println("Status: " + layer.getStatus().getValue());
}

{{< /highlight >}}

