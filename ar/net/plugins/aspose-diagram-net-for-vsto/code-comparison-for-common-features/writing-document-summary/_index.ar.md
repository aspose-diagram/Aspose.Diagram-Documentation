---
title: كتابة ملخص الوثيقة
type: docs
weight: 70
url: /ar/net/writing-document-summary/
---
## **VSTO**
يوجد أدناه كود كتابة ملخص الوثيقة Visio:

{{< highlight "cs" >}}

  Application.ActiveDocument.Creator = "Zeeshan";

 Application.ActiveDocument.Company = "Aspose";

 Application.ActiveDocument.Category = "Drawing 2D";

 Application.ActiveDocument.Manager = "Self";

 Application.ActiveDocument.Title = "Zeeshan";

 Application.ActiveDocument.Subject = "Visio Diagram";


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

يتيح لك Microsoft Visio تحديد عدد من خصائص معلومات ملخص المستند لمساعدتك وزملاؤك في تحديد diagram. خصائص الملخص ، على سبيل المثال العنوان والموضوع والمؤلف والوصف ، تجعل العثور على الملف أسهل عند البحث ، ويسهل التعرف عليه عند التصفح الملفات.

{{% /alert %}} 
### **كتابة Microsoft Visio معلومات ملخص المستند**
 ال[خصائص المستند](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties)تعرض فئة عددًا من الخصائص لتعيين معلومات تلخيصية Microsoft Visio diagram أو الحصول عليها. يمكن لـ Aspose.Diagram for .NET تحديث معلومات ملخص الرسم ثم إعادة كتابة ملف الرسم إلى VDX.

لتحديث معلومات ملخص الرسم لملف VDX أو VSD موجود:

1.  قم بإنشاء مثيل لـ[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) صف دراسي.
1. قم بتعيين الخصائص المعروضة بواسطة Diagram.DocumentProps لتعريف معلومات التلخيص لملف الرسم Visio.
1. قم باستدعاء الأسلوب Save للفئة Diagram لكتابة ملف الرسم Visio إلى VDX.

تحقق من المعلومات الموجزة:

1. افتح ملف الإخراج VDX في Microsoft Visio.
1.  التحديد**معلومات** من**ملف** قائمة.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram("Drawing1.vdx");

 //Set some summary information about the diagram

 vdxDiagram.DocumentProps.Creator = "Ijaz";

 vdxDiagram.DocumentProps.Company = "Aspose";

 vdxDiagram.DocumentProps.Category = "Drawing 2D";

 vdxDiagram.DocumentProps.Manager = "Sergey Polshkov";

 vdxDiagram.DocumentProps.Title = "Aspose Title";

 vdxDiagram.DocumentProps.TimeCreated = DateTime.Now;

 vdxDiagram.DocumentProps.Subject = "Visio Diagram";

 vdxDiagram.DocumentProps.Template = "Aspose Template";

 //Write the updated file to the disk in VDX file format

 vdxDiagram.Save("output.vdx", SaveFileFormat.VDX);


{{< /highlight >}}
## **تنزيل نموذج التعليمات البرمجية**
- [جيثب](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **قم بتنزيل كود التشغيل**
- [جيثب](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Writing%20Document%20Summary)
