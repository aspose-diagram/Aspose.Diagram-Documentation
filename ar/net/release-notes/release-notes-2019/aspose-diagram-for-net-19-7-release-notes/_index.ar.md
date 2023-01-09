---
title: Aspose.Diagram for .NET 19.7 ملاحظات الإصدار
type: docs
weight: 60
url: /ar/net/aspose-diagram-for-net-19-7-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 19.7](https://www.nuget.org/packages/Aspose.Diagram/19.7.0)

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51219|احصل على صور من المعاينة قبل الطباعة لصفحة Visio|التعزيز|
|DIAGRAMNET-51615|قم بتقسيم Diagram إلى صفحات متعددة أثناء تكوين وثيقة PDF|التعزيز|
|DIAGRAMNET-51656|أضف دعمًا لمراقبة تقدم تحويل المستند|التعزيز|
|DIAGRAMNET-50045|فواصل الأسطر غير صحيحة عند تحويل VSD إلى تنسيق PDF|حشرة|
|DIAGRAMNET-50075|VSD إلى PDF التحويل ، خط نص غير صحيح|حشرة|
|DIAGRAMNET-50201|من VSD إلى PDF ، يتم وضع الأشكال في غير مكانها|حشرة|
|DIAGRAMNET-50274|VSDX إلى SVG ، تخطيطات الاتصال غير صحيحة|حشرة|
|DIAGRAMNET-51172|لا يتم تغيير حجم الشكل بشكل صحيح عند الحفظ بتنسيق صورة|حشرة|
|DIAGRAMNET-51613|خاصية AutoFitPageToDrawingContent لا تعمل كما هو متوقع|حشرة|
|DIAGRAMNET-51657|من VISIO إلى JPG - صورة الإخراج ليست بالتنسيق الصحيح|حشرة|
|DIAGRAMNET-51658|تلف VSDX بعد إزالة النسق غير المستخدم|حشرة|
|DIAGRAMNET-51659|تختفي الخلفية أثناء إزالة السمات غير المستخدمة|حشرة|
|DIAGRAMNET-51660|تختفي الأشكال بعد إزالة النسق غير المستخدم|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف SplitMultiPages في PdfSaveOptions**
{{< highlight "java" >}}

 Aspose.Diagram.Saving.PdfSaveOptions o = new Aspose.Diagram.Saving.PdfSaveOptions();

o.SplitMultiPages = true;

diagram.Save("c:\\out.pdf", o);

{{< /highlight >}}
### **يضيف PageSavingCallback في PdfSaveOptions**
{{< highlight "java" >}}

 Aspose.Diagram.Saving.PdfSaveOptions od = new Aspose.Diagram.Saving.PdfSaveOptions();

od.PageSavingCallback = new TestDiagramPageSavingCallback();

d.Save("c:\\test.pdf", od);

{{< /highlight >}}

{{< highlight "java" >}}

 public class TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback

{

    public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)

    {

        Console.WriteLine("Start saving diagram page {0} of pages {1}", args.PageIndex + 1, args.PageCount);

    }

    public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)

    {

        Console.WriteLine("End saving diagram page {0} of pages {1}", args.PageIndex + 1, args.PageCount);

        //don't output pages after page index 8.

        if (args.PageIndex >= 8)

        {

            args.HasMorePages = false;

        }

    }

}

{{< /highlight >}}




