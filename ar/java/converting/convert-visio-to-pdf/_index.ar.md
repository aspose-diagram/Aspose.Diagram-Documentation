---
title:  تحويل Visio إلى تنسيق PDF
linktitle: تحويل Visio إلى PDF
type: docs
weight: 10
url: /ar/java/convert-visio-to-pdf/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل Visio إلى تنسيقات PDF. قم بتحويل VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، VSDM، VSTM،VSSM إلى PDF ببضعة سطور من التعليمات البرمجية.
---
## **التصدير إلى PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Java يكتب مباشرة المعلومات حول API ورقم الإصدار في وثائق المخرجات. على سبيل المثال ، عند تحويل رسم إلى PDF ، يتم تعبئة Aspose.Diagram for Java**طلب**حقل بقيمة "Aspose.Diagram" و**منتج PDF**حقل بقيمة ، على سبيل المثال "Aspose.Diagram 17.9".

يرجى ملاحظة أنه لا يمكنك توجيه Aspose.Diagram for Java API لتغيير أو إزالة هذه المعلومات من مستندات الإخراج.

{{% /alert %}}

 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى PDF باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 استخدم ال[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) مُنشئ class لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

توضح الصورة أدناه VSD diagram أن قصاصات التعليمات البرمجية الموجودة أسفل تصدير PDF. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSX ، VSSM ، VDX ، VST ، VSTX ، VSTM ، VDX ، VTX أو VSX) أيضًا.

**الملف المصدر.**

![ما يجب القيام به: image_بديل_نص](how-to-convert-a-visio-diagram_1.png)

لتصدير VSD diagram إلى PDF:

1. قم بتكوين نسخة من الفئة Diagram.
1. اتصل على Diagram classs Save method واضبط تنسيق الإخراج على PDF.

يوجد أدناه صورة لملف PDF الناتج.

**ملف PDF الناتج.**

![ما يجب القيام به: image_بديل_نص](how-to-convert-a-visio-diagram_2.png)
### **تصدير إلى نموذج برمجة PDF**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToPDF.class);

// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToPDF.vsd");

// Save as PDF file format
diagram.save(dataDir + "ExportToPDF_Out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
```
### **تقسيم عدة صفحات**
Aspose.Diagram for Java يسمح بتقسيم صفحات متعددة أثناء تحويل Microsoft Visio Diagram إلى PDF. يوضح مقتطف الشفرة التالي الوظيفة.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(UsePDFSaveOptions.class);      
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Network Diagram_start.vsdx");
// Options when saving a diagram into the PDF format
PdfSaveOptions options = new PdfSaveOptions();
// set SplitMultiPages option
options.setSplitMultiPages(true);
// save in PDF format
diagram.save(dataDir + "SplitMultiPages.pdf", options);

{{< /highlight >}}
```
### **استخدم استدعاء حفظ الصفحة**
في حالة وجود صفحات متعددة ، يسمح Aspose.Diagram for Java باستخدام خاصية استعادة الصفحة أثناء تحويل Microsoft Visio Diagram إلى PDF. يوضح مقتطف الشفرة التالي الوظيفة.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DocumentConversionProgress.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance PDF save options class
PdfSaveOptions options = new PdfSaveOptions();
          
//set page saving call back
options.setPageSavingCallback( new TestDiagramPageSavingCallback());

// save Visio drawing
diagram.save(dataDir + "Callback_out.pdf", options);

{{< /highlight >}}
```

#### **فئة TestDiagramPageSavingCallback**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
import com.aspose.diagram.IPageSavingCallback;
import com.aspose.diagram.PageEndSavingArgs;
import com.aspose.diagram.PageStartSavingArgs;

public class TestDiagramPageSavingCallback implements IPageSavingCallback
{
    public void pageStartSaving(PageStartSavingArgs args)
    {
    	System.out.println("Start saving page index " + args.getPageIndex() + " of pages " + args.getPageCount());
    }

    public void pageEndSaving(PageEndSavingArgs args)
    {
    	System.out.println("End saving page index " + args.getPageIndex() + " of pages " + args.getPageCount());

        //don't output pages after page index 8.
        if (args.getPageIndex() >= 8)
        {
            args.setHasMorePages(false);
        }
    }
}


{{< /highlight >}}
```
