---
title: بيئة الإعداد وإرشادات التثبيت
type: docs
weight: 20
url: /ar/python-java/setup-environment-and-installation-guidelines/
aliases: [/java/aspose-diagram-for-python-via-java-system-requirements/, /pythonjava/system-requirements/]
keywords: python, visio, instal
description: الإعداد Aspose.Diagram لـ Python عبر Java وإرشادات التثبيت
---
## **متطلبات النظام**
 Aspose.Diagram لـ Python عبر Java هو API مستقل عن النظام الأساسي ويمكن استخدامه على أي منصة (Windows و Linux و MacOS) حيث[Python](https://www.python.org/downloads/)تم تنصيبه. يجب أن يحتوي الجهاز على Java 8 أو إصدارات أعلى قبل إعداد التثبيت.

## **إصدار Python**
- Python 3.5 أو أعلى
## **إصدار Java**
- Java 1.8 أو أعلى

## **Windows:**
### **قم بتثبيت Java وإضافته إلى متغير بيئة PATH**
فمثلا:
{{< highlight "java" >}}

PATH=C:\Program Files\Java\jdk1.8.0_131;

{{< /highlight >}}
  
### **قم بتثبيت Aspose.Diagram لـ Python عبر Java من pypi**
 يمكنك بسهولة استخدام Aspose.Diagram لـ Python عبر Java من[pypi](https://pypi.org/project/aspose-diagram/) بالأمر التالي.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **اختبر Aspose.Diagram للحصول على Python عبر Java**
-  قم بإنشاء ملف باسم**example.py**واستخدم نموذج التعليمات البرمجية التالي:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- الآن قم بتشغيل "python example.py" موجه الأوامر @ لتشغيله.

## **لينكس:**
### **قم بتثبيت Java**
  
### **قم بتثبيت Aspose.Diagram لـ Python عبر Java من pypi**
 يمكنك بسهولة استخدام Aspose.Diagram لـ Python عبر Java من[pypi](https://pypi.org/project/aspose-diagram/) بالأمر التالي.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **اختبر Aspose.Diagram للحصول على Python عبر Java**
-  قم بإنشاء ملف باسم**example.py**واستخدم نموذج التعليمات البرمجية التالي:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- الآن قم بتشغيل "python example.py" موجه الأوامر @ لتشغيله.

## **macOS:**
### **قم بتثبيت Java**
  
### **قم بتثبيت Aspose.Diagram لـ Python عبر Java من pypi**
 يمكنك بسهولة استخدام Aspose.Diagram لـ Python عبر Java من[pypi](https://pypi.org/project/aspose-diagram/) بالأمر التالي.
{{< highlight "java" >}}

 $ pip install aspose-diagram

{{< /highlight >}}

### **اختبر Aspose.Diagram للحصول على Python عبر Java**
-  قم بإنشاء ملف باسم**example.py**واستخدم نموذج التعليمات البرمجية التالي:

{{< highlight "java" >}}

import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

diagram = Diagram()
diagram.save("output.vsdx",SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

- الآن قم بتشغيل "python example.py" موجه الأوامر @ لتشغيله.

