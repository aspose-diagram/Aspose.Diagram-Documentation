---
title: تتبع تقدم تحويل المستند
type: docs
weight: 970
url: /ar/net/track-document-conversion-progress/
description: يشرح هذا القسم كيفية تتبع تقدم التحويل لملفات visio باستخدام Aspose.Diagram.
---
## **سيناريوهات الاستخدام الممكنة**

 في بعض الأحيان ، قد يستغرق تحويل ملفات visio الكبيرة بعض الوقت. خلال هذا الوقت ، قد ترغب في إظهار تقدم تحويل المستند بدلاً من مجرد شاشة تحميل لتحسين إمكانية استخدام التطبيق الخاص بك. Aspose.Diagram يدعم تتبع عملية تحويل الوثيقة من خلال توفير**[IPageSavingCallback] (https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)** واجهه المستخدم. ال**[IPageSavingCallback] (https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**يوفر واجهة**[PageStartSaving] (https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pagestartsaving)**و**[PageEndSaving] (https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pageendsaving)**الطرق التي يمكنك تنفيذها في فئتك المخصصة. يمكنك أيضًا التحكم في الصفحات التي يتم عرضها كما هو موضح في حرف T.*estDiagramPageSavingCallback*فئة مخصصة.

## **تتبع تقدم تحويل المستند**

 نموذج التعليمات البرمجية التالي بتحميل[المصدر visio ملف](Drawing1.vsdx) ويطبع تقدم التحويل في وحدة التحكم باستخدام ملف*TestPageSavingCallback* فئة مخصصة تنفذ**[IPageSavingCallback] (https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**واجهه المستخدم.

## **عينة من الرموز**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance PDF save options class
Aspose.Diagram.Saving.PdfSaveOptions options = new Aspose.Diagram.Saving.PdfSaveOptions();
          
//set page saving call back
options.PageSavingCallback = new TestDiagramPageSavingCallback();

// save Visio drawing
diagram.Save(dataDir + "Callback_out.pdf", options);

{{< /highlight >}}


ما يلي هو رمز*TestDiagramPageSavingCallback*فئة مخصصة.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
public class TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback
{
    public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)
    {
        Console.WriteLine("Start saving diagram page index {0} of pages {1}", args.PageIndex, args.PageCount);
    }

    public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)
    {
        Console.WriteLine("End saving diagram page index {0} of pages {1}", args.PageIndex, args.PageCount);

        //don't output pages after page index 8.
        if (args.PageIndex >= 8)
        {
            args.HasMorePages = false;
        }
    }
}

{{< /highlight >}}


## **إخراج وحدة التحكم**

ابدأ بحفظ فهرس الصفحة 0 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 0 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 1 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 1 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 2 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 2 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 3 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 3 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 4 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 4 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 5 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 5 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 6 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 6 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 7 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 7 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 8 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 8 من الصفحات 11
