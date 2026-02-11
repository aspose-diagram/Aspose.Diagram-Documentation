---
title:  تحويل Visio إلى تنسيقات الصور
linktitle: تحويل Visio إلى صور
type: docs
weight: 20
url: /ar/python-java/convert-visio-to-image/
description: يوضح هذا الموضوع كيفية تحويل Visio إلى تنسيقات صور متنوعة باستخدام Aspose.Diagram لـ Python via Java. تحويل Visio،VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، JPEG، VSTX صورة بضعة أسطر من التعليمات البرمجية.
---
## **تصدير المخططات إلى تنسيقات ملفات الصور**
يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى صورة باستخدام Aspose.Diagram لـ Python via Java.

استخدم مُنشئ الفئة Diagram لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم. تُظهر الصورة أدناه ملف VSD على وشك أن يتم حفظه بتنسيق PNG. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSX ، VSSM ، VDX ، VST ، VSTX ، VSTM ، VDX ، VTX أو VSX) أيضًا.

**[على سبيل المثال ملف VSD.] (ExportToImage.vsd)**

لتصدير diagram إلى صورة:

- قم بتكوين نسخة من الفئة Diagram.
- اتصل بـ Diagram class 'Save method وقم بتعيين تنسيق الصورة الذي تريد التصدير إليه ، ملف صورة الإخراج يبدو مثل الملف الأصلي.

**ملف الإخراج PNG.**

![ما يجب القيام به: image_بديل_نص](ExportToImage.png)
### **التصدير إلى نموذج برمجة ملفات الصور**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
diagram = Diagram("ExportToImage.vsd")

# Save as PNG
diagram.save("ExportToImage_Out.png", SaveFileFormat.PNG)

jpype.shutdownJVM()

{{< /highlight >}}
```

من الممكن أيضًا حفظ صفحة معينة على الصورة ، بدلاً من حفظ المستند بأكمله:

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("ExportToImage.vsd")

# Save diagram as PNG
options = ImageSaveOptions(SaveFileFormat.PNG)

# Save one page only, by page index
options.setPageIndex(0)

# Save resultant Image file
diagram.save("ExportPageToImage_Out.png", options)

jpype.shutdownJVM()

{{< /highlight >}}
```