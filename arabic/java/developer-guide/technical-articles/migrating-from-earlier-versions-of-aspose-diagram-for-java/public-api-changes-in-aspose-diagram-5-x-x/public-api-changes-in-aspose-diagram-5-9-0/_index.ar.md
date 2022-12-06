---
title: API العام التغييرات في Aspose.Diagram 5.9.0
type: docs
weight: 10
url: /ar/java/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 5.8.0 إلى 5.9.0 ، والتي قد تهم مطوري الوحدة / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
### **حفظ HTML الناتج في دفق**
تمت إضافة طريقة الحفظ الجديدة في فئة Diagram. يأخذ معلمتين ، كائن الدفق وتنسيق ملف الحفظ.
رمز المثال:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

ByteArrayOutputStream dstStream = new ByteArrayOutputStream();

diagram.save(dstStream, SaveFileFormat.HTML);

// In you want to read the result into a Diagram object again, in Java you need to get the

// data bytes and wrap into an input stream.

ByteArrayInputStream srcStream = new ByteArrayInputStream(dstStream.toByteArray());

{{< /highlight >}}
### **نسخ السمات وورقة الصفحة من Visio آخر**
توفر فئة Diagram طريقة CopyTheme وفئة PageSheet تقدم طريقة Copy لتحقيق هدف نسخ شكل ومهام معالجة أخرى.
 رموز المثال:[نسخ الأشكال من Visio موجود](/diagram/ar/java/working-with-visio-shape-data/#copy-shapes-from-an-existing-visio)
### **تمت إضافة خيارات الحفظ VSTX و VSSX في SaveFileFormat**
في السابق ، كان Aspose.Diagram API يدعم القراءة والكتابة بتنسيق VSDX ، لكننا الآن أضفنا دعمًا لكتابة المخططات بتنسيقات VSTX و VSSX أيضًا. رموز المثال:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}
### **تمت إضافة خيار القراءة VSSX في LoadFileFormat**
في السابق ، كان Aspose.Diagram API يدعم القراءة والكتابة بتنسيق VSDX ، لكننا الآن أضفنا دعمًا لقراءة تنسيق استنسل VSSX أيضًا. رموز المثال:

**Java**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram("C:\\temp\\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}
