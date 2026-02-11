---
title: أول طلب Aspose.Diagram - Hello World
type: docs
weight: 30
url: /ar/python-java/your-first-aspose-diagram-application-hello-world/
description: توضح هذه الصفحة كيفية إنشاء التطبيق الأول باستخدام مكتبة Aspose.Diagram.
---
{{% alert color="primary" %}}

يوضح هذا البرنامج التعليمي كيفية إنشاء أول تطبيق (Hello World) باستخدام Aspose.Diagram "API البسيط. يقوم هذا التطبيق البسيط بإنشاء ملف Microsoft Visio بالنص" Hello World "في صفحة محددة.

{{% /alert %}}

## **إنشاء تطبيق Hello World**

تؤدي الخطوات أدناه إلى إنشاء تطبيق Hello World باستخدام Aspose.Diagram API:

1. قم بتكوين نسخة من الفئة Diagram.
1. تطبيق الرخصة:
 1. إذا كنت قد اشتريت ترخيصًا ، فاستخدم الترخيص الموجود في التطبيق الخاص بك للوصول إلى الوظائف الكاملة Aspose.Diagram
 1. إذا كنت تستخدم الإصدار التقييمي للمكون (إذا كنت تستخدم Aspose.Diagram بدون ترخيص) ، فتخط هذه الخطوة.
1. قم بتكوين ملف Visio جديد ، أو افتح ملف Visio موجود.
1. قم بإنشاء مربع نص جديد.
1.  أدخل الكلمات**Hello World!** في مربع نص.
1. قم بإنشاء ملف Microsoft Visio المعدل.

يتم توضيح تنفيذ الخطوات المذكورة أعلاه في الأمثلة أدناه.

### **نموذج التعليمات البرمجية: إنشاء Diagram جديد وكتابة Hello World!**

يفتح المثال التالي ملف قالب Microsoft Visio موجود باسم "[Basic_Shapes.vss](Basic_Shapes.vss)"، يدخل نص" Hello World! "في الصفحة الأولى ويحفظ diagram.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

diagram = Diagram("Basic_Shapes.vss")

# Add a new hello world rectangle shape
shapeId = diagram.addShape(4.25, 5.5, 2, 1, "Rectangle", 0)
shape = diagram.getPages().getPage(0).getShapes().getShape(shapeId)
shape.getText().getValue().add(Txt("Hello World"))

# Save diagram in the VSDX format
diagram.save("CreateHelloWorldVisio_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

