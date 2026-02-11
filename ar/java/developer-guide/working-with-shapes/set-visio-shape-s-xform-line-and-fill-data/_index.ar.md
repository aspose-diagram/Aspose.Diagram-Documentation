---
title: قم بتعيين Visio شكل XForm و Line و Fill Data
type: docs
weight: 70
url: /ar/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **ضبط بيانات XForm**
 عنصر XForm هو جزء من Microsoft Visio مخطط XML. يحدد XForm موضع الأشكال ، على سبيل المثال العرض والارتفاع والدوران وما إذا كان الشكل قد انعكس. ال[XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) الممتلكات التي يتعرض لها[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) فئة ، يدعم كائن Aspose.Diagram.XForm. يمكن استخدام الخاصية XForm لاسترداد بيانات XForm للشكل أو تحديثها. تعمل أمثلة التعليمات البرمجية في هذه المقالة على تغيير قيم PinX (إحداثيات س) و PinY (إحداثيات ص) لتحريك الأشكال على الصفحة.

**المدخلات diagram** 

![ما يجب القيام به: image_بديل_نص](set-visio-shape-s-xform-line-and-fill-data_1.png)

**diagram بعد** **PinX** **و** **بيني** **تم تغيير القيم** 

![ما يجب القيام به: image_بديل_نص](set-visio-shape-s-xform-line-and-fill-data_2.png)

عملية تحديث بيانات XForm هي:

1. قم بتحميل diagram. # ابحث عن شكل معين # قم بتحديث بيانات XForm للشكل.
1. احفظ diagram.
### **عينة البرمجة**
يوضح مقتطف الشفرة أدناه كيفية تحديث بيانات XForm للشكل. يبحث الكود عن عملية أسماء الأشكال ، بمعرف الشكل 1 ، ويضبط إحداثياته X و Y على 5.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetXFormdata.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

//Find a particular shape and update its XForm
for(Shape shape :(Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)
    {
        shape.getXForm().getPinX().setValue(5);
        shape.getXForm().getPinY().setValue(5);
    }
}
// save diagram
diagram.save(dataDir + "SetXFormdata_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **قم بتعيين Visio بيانات خط الشكل**
يمكن تنسيق الأشكال بعدة طرق. توضح هذه المقالة كيفية تحديد سمات السطر.

Microsoft Visio يتيح للمستخدمين تنسيق السطور بعدة طرق. Aspose.Diagram for Java يدعم:

- الوزن: سمك الخط.
- اللون: تعيين لون خط الشكل.
- شفافية لون الخط: اضبط شفافية لون خط الشكل بالنسبة المئوية.
- النمط: يحدد ما إذا كان الخط متصلًا أم متقطعًا أم له نمط آخر.
- التقريب: نصف قطر الزوايا.
- أسهم البداية والنهاية: تحدد ما إذا كان السطر يحتوي على أسهم أم لا.
- أحجام أسهم البداية والنهاية: قم بتعيين أحجام الأسهم.
- الغطاء: تقريب الخط ينتهي.
### **تغيير لون الخط والوزن ونوع الشرطة والشفافية والتقريب ونوع السهم وحجم السهم لحد الشكل**
 ال[خط](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) الممتلكات التي يتعرض لها[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)فئة ، تدعم كائن Aspose.Diagram.Line. يمكن استخدام هذه الخاصية لاسترداد بيانات خط الشكل أو تحديثها.
#### **عينة برمجة بيانات الخط**
يقوم الجزء التالي من التعليمات البرمجية بتحديث بيانات خط الشكل.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetLineData.class);

// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// get the page by its name
Page page1 = diagram.getPages().getPage("Page-1");
// get shape by its ID
Shape shape = page1.getShapes().getShape(1);
// set line dash type by index
shape.getLine().getLinePattern().setValue(4);
// set line weight, defualt in PT
shape.getLine().getLineWeight().setValue(2);
// set color of the shape's line
shape.getLine().getLineColor().getUfe().setF("RGB(95,108,53)");
// set line rounding, default in inch
shape.getLine().getRounding().setValue(0.3125);
// set line caps
shape.getLine().getLineCap().setValue(BOOL.TRUE);
// set line color transparency in percent
shape.getLine().getLineColorTrans().setValue(50);

/* add arrows to the connector or curve shapes */
// select arrow type by index
shape.getLine().getBeginArrow().setValue(4);
shape.getLine().getEndArrow().setValue(4);
// set arrow size 
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);

// save the Visio
diagram.save(dataDir + "SetLineData_Out.vsdx", SaveFileFormat.VSDX);
// save diagram
diagram.save(dataDir+ "output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **قم بتعيين Visio بيانات تعبئة الشكل**
يمكن تنسيق الأشكال بعدة طرق. يصف هذا الموضوع كيفية تحديد تعبئة الشكل.

 Microsoft Office Visio يتيح للمستخدمين تنسيق التعبئة بطرق مختلفة. ال[يملأ](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) فئة Aspose.Diagram for Java API تدعم الإعداد:

- ألوان الخلفية والمقدمة.
- الشفافية.
- أنماط التعبئة.
- الظلال.
### **ضبط قيم التعبئة**
تدعم خاصية Fill ، المكشوفة بواسطة فئة Shape ، كائن Aspose.Diagram.Fill. يمكن استخدام الخاصية Fill لاسترداد بيانات تعبئة الشكل أو تحديثها.

|<p>**المدخلات diagram** </p><p>![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/OrhEecb.png)</p>|<p>**diagram بعد تغيير لون التعبئة** </p><p>![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **تعبئة نموذج لبرمجة البيانات**
يقوم مقتطف التعليمات البرمجية التالي بتحديث بيانات تعبئة الشكل. تبحث الشفرة عن شكل يسمى مستطيل ، بمعرف الشكل 1 ، وتعيين خلفية التعبئة وألوان المقدمة.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetFillData.class);


//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir+ "Drawing1.vsd");

//Find a particular shape and update its XForm
for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "rectangle" && shape.getID() == 1)
    {
        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue());
        shape.getFill().getFillForegnd().setValue("#ebf8df");
    }
}
// save diagram
diagram.save(dataDir+ "SetFillData_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **استرجع بيانات التعبئة الموروثة لشكل Visio**
يمكن أن ترث أشكال Visio النمط الأصل والشكل الرئيسي. يمكن للمطورين الحصول على بيانات التعبئة الموروثة لشكل Visio أو تعيينها. تحتوي الخاصية InheritFill ، المكشوفة بواسطة فئة الشكل ، على قيم تنسيق التعبئة للشكل الذي يرثه النمط الأصل والشكل الرئيسي.
#### **استرجاع نموذج برمجة بيانات التعبئة الموروثة**
يسترد مقتطف التعليمات البرمجية التالي بيانات التعبئة الموروثة للشكل. يرجى التحقق من نموذج الكود هذا:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}
```
