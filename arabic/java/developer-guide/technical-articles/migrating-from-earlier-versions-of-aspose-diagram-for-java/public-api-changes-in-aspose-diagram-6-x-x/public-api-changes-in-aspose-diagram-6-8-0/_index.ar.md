---
title: API العام التغييرات في Aspose.Diagram 6.8.0
type: docs
weight: 10
url: /ar/java/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 6.7.0 إلى 6.8.0 ، والتي قد تهم مطوري الوحدة / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
### **أدخل عنصر تحكم ActiveX**
 يمكن للمطورين إدراج عنصر تحكم ActiveX في Visio diagram. لقد أضفنا طريقة addActiveXControl في[صفحة](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page) صف دراسي. الرجاء التحقق من مثال هذا الرمز:

**Java**

{{< highlight "java" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);

// save diagram

diagram.save("C:\\temp\\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **قم بتعيين Color CheckBox of Layer**
يمكن للمطورين تعيين أو الحصول على Color CheckBox of Layer باستخدام Aspose.Diagram API. يرجى التحقق من مثال الكود هذا:

**Java**

{{< highlight "java" >}}

 // Load source Visio diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// Get Visio page

Page page = diagram.getPages().getPage("Page-1");

// Initialize a new Layer class object

Layer layer = new Layer();

// set Layer name

layer.getName().setValue("Layer1");

// Set Layer Visibility

layer.getVisible().setValue(BOOL.TRUE);

// set the color checkbox of Layer

layer.setColorChecked(BOOL.TRUE);

// Add Layer to the particular page sheet

page.getPageSheet().getLayers().add(layer);

// get shape by ID

Shape shape = page.getShapes().getShape(3);

// assign shape to this new Layer

shape.getLayerMem().getLayerMember().setValue(Integer.toString(layer.getIX()));

// save diagram

diagram.save("c:\\temp\\AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **يضيف خاصية InheritFill في فئة الشكل**
يمكن للمطورين الحصول على خاصية التعبئة الموروثة أو تعيينها. لقد أضفنا خاصية InheritFill في فئة Shape. الرجاء التحقق من مثال هذا الرمز:

**Java**

{{< highlight "java" >}}

 // call the diagram constructor to load a VSDX diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// get page by ID

Page page = diagram.getPages().getPage("Page-1");

// get shape by ID

Shape shape = page.getShapes().getShape(1);

// get the fill formatting values

System.out.println(shape.getInheritFill().getFillBkgnd().getValue());

System.out.println(shape.getInheritFill().getFillForegnd().getValue());

System.out.println(shape.getInheritFill().getFillPattern().getValue());

{{< /highlight >}}
