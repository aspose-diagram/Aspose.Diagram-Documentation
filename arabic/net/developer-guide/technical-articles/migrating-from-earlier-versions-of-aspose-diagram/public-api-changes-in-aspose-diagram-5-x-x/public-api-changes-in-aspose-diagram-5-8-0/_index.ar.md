---
title: API العام التغييرات في Aspose.Diagram 5.8.0
type: docs
weight: 20
url: /ar/net/public-api-changes-in-aspose-diagram-5-8-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 5.7.0 إلى 5.8.0 ، والتي قد تهم مطوري الوحدة / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
## **تمت إضافة خيار SaveToolBar في HTMLSaveOptions**
تمت إضافة خيار SaveToolBar الجديد في فئة HTMLSaveOptions. تحدد ما إذا كنت تريد حفظ شريط الأدوات أم لا. القيمة الافتراضية هي الحقيقية. رموز المثال:

**C#**

{{< highlight "java" >}}

 // initialize HTMLSaveOptions class object

HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option

opts.SaveToolBar = false;

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' initialize HTMLSaveOptions class object

Dim opts As New HTMLSaveOptions()

' set save toolbar option

opts.SaveToolBar = False

{{< /highlight >}}
## **VSDX تم اضافة خيار الحفظ في SaveFileFormat**
في السابق ، كان Aspose.Diagram API يدعم قراءة تنسيق VSDX ، لكننا الآن أضفنا دعمًا لكتابة المخططات بتنسيق VSDX. رموز المثال:

**C#**

{{< highlight "java" >}}

 // save diagram in the VSDX format

diagram.Save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' save diagram in the VSDX format

diagram.Save("C:\temp\Output.vsdx", SaveFileFormat.VSDX)

{{< /highlight >}}
## **تمت إضافة أسلوب المجموعة في فئة ShapeCollection**
يمكن للمطورين الآن تجميع عدة أشكال معًا في Visio diagram باستخدام Aspose.Diagram API.

**C#**

{{< highlight "java" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(@"c:\temp\test.vdx");

// Initialize an array of shapes

Aspose.Diagram.Shape[]ss = new Aspose.Diagram.Shape[2];

// extract and assign shapes to the array

ss[0]= diagram.Pages[0].Shapes.GetShape(1);

ss[1]= diagram.Pages[0].Shapes.GetShape(2);

// mark array shapes as group

diagram.Pages[0].Shapes.Group(ss);

// save visio diagram

diagram.Save(@"c:\temp\out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' load a Visio diagram

Dim diagram As New Diagram("c:\temp\test.vdx")

' Initialize an array of shapes

Dim ss As Aspose.Diagram.Shape() = New Aspose.Diagram.Shape(1) {}

' extract and assign shapes to the array

ss(0) = diagram.Pages(0).Shapes.GetShape(1)

ss(1) = diagram.Pages(0).Shapes.GetShape(2)

' mark array shapes as group

diagram.Pages(0).Shapes.Group(ss)

' save visio diagram

diagram.Save("c:\temp\out.vsdx", SaveFileFormat.VSDX)

{{< /highlight >}}
