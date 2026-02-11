---
title: تصغير حجم الملف
type: docs
weight: 50
url: /ar/python-java/reduce-file-size/
description: يشرح هذا القسم كيفية تصغير حجم الملف من diagram مع Aspose.Diagram لـ Python via Java.
---
## **تصغير حجم الملف**
 Aspose.Diagram لـ Python via Java API يسمح للمطورين بإزالة المعلومات المخفية من diagram لتقليل حجم الملف.
 يمثل كائن الصفحة منطقة الرسم لصفحة أمامية أو صفحة خلفية. لتقليل حجم الملف ، يمكنك استخدام خصائص RemoveHiddenInfoItem في**RemoveHiddenInformation ()** طريقة Diagram فئة. يوضح مثال الكود أدناه كيفية إزالة المعلومات المخفية من diagram.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load a Visio diagram
diagram = Diagram("Drawing1.vsdx")

# Remove hidden information from diagram
diagram.removeHiddenInformation(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS)

# save in the VSDX format
diagram.save("ReduceFileSize_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

