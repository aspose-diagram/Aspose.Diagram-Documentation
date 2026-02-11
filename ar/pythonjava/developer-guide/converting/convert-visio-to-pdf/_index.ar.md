---
title:  تحويل Visio إلى PDF تنسيق
linktitle: حوّل Visio إلى PDF
type: docs
weight: 10
url: /ar/python-java/convert-visio-to-pdf/
description: يوضح لك هذا الموضوع كيفية تحويل تنسيقات Visio إلى PDF باستخدام Aspose.Diagram لـ Python via Java. قم بتحويل VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، VSDM، VSTX، VSDM أسطر.
---
## **تصدير الى PDF**
{{% alert color="primary" %}}

يقوم Aspose.Diagram لـ Python via Java بكتابة المعلومات حول API ورقم الإصدار مباشرةً في مستندات الإخراج. على سبيل المثال ، عند تقديم رسم إلى PDF ، يتم تعبئة Aspose.Diagram for Java**طلب**حقل بقيمة "Aspose.Diagram" و**PDF منتج**حقل بقيمة ، على سبيل المثال "Aspose.Diagram 17.9".

يرجى ملاحظة أنه لا يمكنك توجيه Aspose.Diagram لـ Python via Java لتغيير أو إزالة هذه المعلومات من مستندات الإخراج.

{{% /alert %}}

توضح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى PDF باستخدام Aspose.Diagram لـ Python via Java.

استخدم مُنشئ الفئة Diagram لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

[VSD diagram](ExportToPDF.vsd)هو مثال لملف الرسم لتصدير PDF. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSX ، VSSM ، VDX ، VST ، VSTX ، VSTM ، VDX ، VTX أو VSX) أيضًا.

لتصدير VSD diagram إلى PDF:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء Diagram classs Save method واضبط تنسيق الإخراج على PDF.

### **التصدير إلى عينة برمجة PDF**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToPDF.vsd")

# Save as PDF file format
diagram.save("ExportToPDF_Out.pdf", SaveFileFormat.PDF)

jpype.shutdownJVM()

{{< /highlight >}}
```

### **تقسيم عدة صفحات**
Aspose.Diagram for Java يسمح بتقسيم صفحات متعددة أثناء تحويل Microsoft Visio Diagram إلى PDF. يوضح مقتطف الكود التالي الوظيفة.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSDX file
diagram = Diagram("Network Diagram_start.vsdx")
# Options when saving a diagram into the PDF format
options = PdfSaveOptions()
# set SplitMultiPages option
options.setSplitMultiPages(True)
# save in PDF format
diagram.save("SplitMultiPages.pdf", options)

jpype.shutdownJVM()

{{< /highlight >}}
```
