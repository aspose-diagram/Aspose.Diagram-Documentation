---
title: API العام التغييرات في Aspose.Diagram 5.9.0
type: docs
weight: 10
url: /ar/net/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 5.8.0 إلى 5.9.0 ، والتي قد تهم مطوري الوحدة / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
## **حفظ HTML الناتج في دفق**
تمت إضافة طريقة Save الجديدة في الفئة Diagram. يأخذ معلمتين ، كائن الدفق وتنسيق ملف الحفظ.
رمز المثال:

**C#**

{{< highlight "java" >}}

 // load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' load an existing visio diagram

Dim diagram As Diagram = New Diagram("Basic Flowchart.vsd")

' save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream()

diagram.Save(stream, SaveFileFormat.HTML)

{{< /highlight >}}
## **نسخ السمات وورقة الصفحة من Visio آخر**
توفر فئة Diagram طريقة CopyTheme وفئة PageSheet تقدم طريقة Copy لتحقيق هدف نسخ شكل ومهام معالجة أخرى.
 رموز المثال:[نسخ الأشكال من Visio موجود](/diagram/ar/net/add-retrieve-copy-and-read-visio-shape-data/)
## **تمت إضافة خيارات الحفظ VSTX و VSSX في SaveFileFormat**
في السابق ، كان Aspose.Diagram API يدعم القراءة والكتابة بتنسيق VSDX ، لكننا الآن أضفنا دعمًا لكتابة المخططات بتنسيقات VSTX و VSSX أيضًا. رموز المثال:

**C#**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX)

' save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX)

{{< /highlight >}}
## **تمت إضافة خيار القراءة VSSX في LoadFileFormat**
في السابق ، كان Aspose.Diagram API يدعم القراءة والكتابة بتنسيق VSDX ، لكننا الآن أضفنا دعمًا لقراءة تنسيق استنسل VSSX أيضًا. رموز المثال:

**C#**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX)

{{< /highlight >}}
