---
title: طباعة Diagram في VSTO و Aspose.Diagram
type: docs
weight: 100
url: /ar/net/printing-a-diagram-in-vsto-and-aspose-diagram/
---
## **VSTO**
يوجد أدناه رمز لإظهار كيفية طباعة diagram:

{{< highlight "cs" >}}

   Application.ActiveDocument.Print();

{{< /highlight >}}
## **Aspose.Diagram**
 طباعة diagram إلى**الطابعة الافتراضية** بسيط للغاية في Aspose.Diagram for .NET. نفذ الخطوات التالية لطباعة diagram إلى الطابعة الافتراضية:

- قم بتكوين نسخة من فئة Diagram لتحميل diagram الذي سيتم طباعته
- قم باستدعاء أسلوب الطباعة مع عدم وجود معاملات كما تم كشفها بواسطة الكائن Diagram

 طباعة diagram إلى**طابعة محددة** يتطلب اسم الطابعة كمعامل لطريقة الطباعة لـ Diagram. قم بتنفيذ الخطوات التالية لطباعة diagram إلى الطابعة المطلوبة:

- قم بتكوين نسخة من فئة Diagram لتحميل diagram الذي سيتم طباعته
- قم باستدعاء أسلوب الطباعة للفئة Diagram باستخدام اسم الطابعة كمعامل سلسلة إلى أسلوب الطباعة

فيما يلي رمز استخدام الطابعة الافتراضية والمحددة:

{{< highlight "cs" >}}

  string FilePath = "demo.vsd";

 //Load the diagram

 Diagram diagram = new Diagram(FilePath);

 //Call the print method to print whole Diagram to the default printer

 diagram.Print();

 //Call the print method to print whole Diagram to the desired printer

 diagram.Print("LaserJet1100");

 PrinterSettings settings = new PrinterSettings();

 settings.PrinterName = "LaserJet1100";

 //Call the print method to print whole Diagram to the desired printer and set document name in print job

 diagram.Print(settings, "Job name while printing with Aspose.Diagram");


{{< /highlight >}}
## **تنزيل نموذج التعليمات البرمجية**
- [جيثب](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **قم بتنزيل كود التشغيل**
- [جيثب](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Printing%20a%20Diagram)
