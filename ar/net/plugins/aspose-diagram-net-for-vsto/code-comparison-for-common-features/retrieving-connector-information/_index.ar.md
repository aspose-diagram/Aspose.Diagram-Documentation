---
title: استرداد معلومات الموصل
type: docs
weight: 90
url: /ar/net/retrieving-connector-information/
---
## **VSTO**
يوجد أدناه الرمز للحصول على معلومات الموصل:

{{< highlight "cs" >}}

   foreach (Visio.Connect Connect in Application.ActiveDocument.Pages[1].Connects)

  {

    MessageBox.Show("\nFrom Shape ID : " + Connect.FromSheet);

    MessageBox.Show("To Shape ID : " + Connect.ToSheet);

  }


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 يوفر Aspose.Diagram for .NET آليات لاسترجاع المعلومات - المعرف والاسم - حول[الصفحات](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) و[رئيسي - سيد](https://reference.aspose.com/diagram/net/aspose.diagram/mastercollection). كما يتيح لك الحصول على معلومات حول الموصلات والعناصر التي تربط الأشكال.

{{% /alert %}} 

 ال[الاتصال](https://reference.aspose.com/diagram/net/aspose.diagram/connect) يمثل الكائن الموصل الذي يربط شكلين على Visio صفحة رسم. الخاصية Connects ، المكشوفة بواسطة[صفحة](https://reference.aspose.com/diagram/net/aspose.diagram/page) فئة تدعم مجموعة من Aspose.Diagram.Connect الكائنات. يمكن استخدام هذه الخاصية لاسترداد معلومات المعرف والاسم حول الموصل.

يوجد أدناه الكود للحصول على معلومات الموصل باستخدام Aspose.Diagram .NET:

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Connect connector in vdxDiagram.Pages[1].Connects)

 {

   //Display information about the Connectors

   Console.WriteLine("\nFrom Shape ID : " + connector.FromSheet);

   Console.WriteLine("To Shape ID : " + connector.ToSheet);

 }

 Console.ReadLine();


{{< /highlight >}}
## **تنزيل نموذج التعليمات البرمجية**
- [جيثب](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **قم بتنزيل كود التشغيل**
- [جيثب](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Connector%20Information)
