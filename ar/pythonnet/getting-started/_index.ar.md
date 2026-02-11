---
title: ابدء
linktitle: ابدء
type: docs
weight: 4
url: /ar/python-net/getting-started/ 
keywords: python, visio, instal
description: قم بإعداد Aspose.Diagram لـ Python via .NET وإرشادات التثبيت.
---
## **متطلبات النظام**
 Aspose.Diagram لـ Python via .NET مستقل عن النظام الأساسي API ويمكن استخدامه على أي منصة (Windows و Linux) حيث[Python](https://www.python.org/downloads/) تم تنصيبه.

## **إصدار Python**
- Python 3.6 أو أعلى

## **تثبيت**
### **Windows:**
 يمكنك بسهولة استخدام Aspose.Diagram لـ Python via .NET من[pypi](https://pypi.org/project/aspose-diagram-python/) بالأمر التالي.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

### **لينكس:**
 يمكنك بسهولة استخدام Aspose.Diagram لـ Python via .NET من[pypi](https://pypi.org/project/aspose-diagram-python/) بالأمر التالي.
{{< highlight "NET" >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

## **إنشاء تطبيق Hello World**

-  قم بإنشاء ملف باسم**CreatingNewVisioFile.py** واستخدم نموذج التعليمات البرمجية التالي:


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


- الآن احفظ الكود أعلاه في "CreatingNewVisioFile.py" وقم بتشغيل "python CreatingNewVisioFile.py"command موجه.
