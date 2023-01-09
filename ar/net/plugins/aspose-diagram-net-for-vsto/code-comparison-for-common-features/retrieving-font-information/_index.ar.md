---
title: استرداد معلومات الخط
type: docs
weight: 80
url: /ar/net/retrieving-font-information/
---
## **VSTO**
يوجد أدناه رمز استرداد معلومات الخط:

{{< highlight "cs" >}}

  foreach (Font font in Application.ActiveDocument.Fonts)

 {

    //Display information about the fonts

    MessageBox.Show(font.Name);

 }

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram لديه آليات لاسترجاع المعلومات حول العناصر التي تشكل diagram ، من[الصفحات](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) الإستنسل[موصلات](/diagram/ar/net/retrieving-connector-information/)وكذلك الخطوط. يوضح هذا المقال كيفية معرفة الخطوط المستخدمة في diagram.

{{% /alert %}} 

 ال[الخط](https://reference.aspose.com/diagram/net/aspose.diagram/font) يمثل الكائن محرفًا يتم تطبيقه على نص في مستند أو متاح للاستخدام على النظام.

يقوم كائن الخط بتعيين اسم (على سبيل المثال ، "Arial") لمعرف الخط (على سبيل المثال ، 3) الذي يخزنه Microsoft Visio في خلية خط في قسم حرف لشكل يحتوي على نص منسق باستخدام هذا الخط. يمكن أن تتغير معرفات الخطوط عند فتح مستند على أنظمة مختلفة أو عند تثبيت الخطوط أو إزالتها.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)

 {

    //Display information about the fonts

    Console.WriteLine(font.Name);

 }

{{< /highlight >}}
## **تنزيل نموذج التعليمات البرمجية**
- [جيثب](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **قم بتنزيل كود التشغيل**
- [جيثب](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Font%20Information)
