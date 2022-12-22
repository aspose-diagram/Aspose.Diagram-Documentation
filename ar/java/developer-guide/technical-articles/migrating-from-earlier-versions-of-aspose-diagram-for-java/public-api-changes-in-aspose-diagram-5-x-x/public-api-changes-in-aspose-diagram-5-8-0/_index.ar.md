---
title: API العام التغييرات في Aspose.Diagram 5.8.0
type: docs
weight: 20
url: /ar/java/public-api-changes-in-aspose-diagram-5-8-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 5.7.0 إلى 5.8.0 ، والتي قد تهم مطوري الوحدة / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
### **تمت إضافة خيار SaveToolBar في HTMLSaveOptions**
تمت إضافة خيار SaveToolBar الجديد في فئة HTMLSaveOptions. تحدد ما إذا كنت تريد حفظ شريط الأدوات أم لا. القيمة الافتراضية هي الحقيقية. رموز المثال:

**Java**

{{< highlight "java" >}}

 // initialize HTMLSaveOptions class object

HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option

opts.setSaveToolBar(false);

{{< /highlight >}}
### **VSDX تم اضافة خيار الحفظ في SaveFileFormat**
في السابق ، كان Aspose.Diagram API يدعم قراءة تنسيق VSDX ، لكننا الآن أضفنا دعمًا لكتابة المخططات بتنسيق VSDX. رموز المثال:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSDX format

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **تمت إضافة أسلوب المجموعة في فئة ShapeCollection**
يمكن للمطورين الآن تجميع عدة أشكال معًا في Visio diagram باستخدام Aspose.Diagram API.

**Java**

{{< highlight "java" >}}

 // load a Visio diagram

Diagram diagram = new Diagram("c:\\temp\\test.vsd");

// Initialize an array of shapes

Shape[]shapes = new Shape[2];

// extract and assign shapes to the array

shapes[0]= diagram.getPages().get(0).getShapes().getShape(1);

shapes[1]= diagram.getPages().get(0).getShapes().getShape(2);

// mark array shapes as group

diagram.getPages().get(0).getShapes().group(shapes);

// save visio diagram

diagram.save("c:\\temp\\out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
