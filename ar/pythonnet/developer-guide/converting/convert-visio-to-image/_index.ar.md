---
title:  تحويل Visio إلى تنسيقات الصور
linktitle: تحويل Visio إلى صور
type: docs
weight: 20
url: /ar/python-net/convert-visio-to-image/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل Visio إلى تنسيقات صور مختلفة. تحويل Visio،VSD ، VSS ، VDW ، VST ، VSDX ، VSSX ، VSTX ، VSDM ، VSTM،VSSM إلى PNG ، JPEG ، BMP من الصور.
---
## **تصدير المخططات إلى تنسيقات ملفات الصور**
 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى صورة باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/python-net/) API. استخدم مُنشئ الفئة [Diagram] لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

لتصدير diagram إلى صورة:

- قم بتكوين نسخة من الفئة Diagram.
- اتصل بـ Diagram class 'Save method وقم بتعيين تنسيق الصورة الذي تريد التصدير إليه ، ملف صورة الإخراج يبدو مثل الملف الأصلي.
### **تصدير Microsoft Visio الرسم إلى ملف الصورة**

{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the png format
diagram.save("Visio_out.png", SaveFileFormat.PNG)
{{< /highlight >}}


من الممكن أيضًا حفظ صفحة معينة على الصورة ، بدلاً من حفظ المستند بأكمله:


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save diagram as PNG
options = saving.ImageSaveOptions(SaveFileFormat.PNG)
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the png format
diagram.save("ExportPageToImage_out.png", options)
{{< /highlight >}}
