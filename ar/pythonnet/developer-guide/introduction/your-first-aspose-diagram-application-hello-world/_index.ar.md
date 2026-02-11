---
title: أول طلب Aspose.Diagram - Hello World
type: docs
weight: 30
url: /ar/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

يوضح موضوع المبتدئين هذا كيف يمكن للمطورين إنشاء تطبيق أول بسيط (Hello World) باستخدام Aspose.Diagram 'بسيط API. يقوم التطبيق بإنشاء ملف Microsoft Visio بالكلمات Hello World في الصفحة.

{{% /alert %}}

### **إنشاء تطبيق Hello World**

لإنشاء تطبيق Hello World باستخدام Aspose.Diagram API:

1. قم بإنشاء مثيل لفئة المصنف.
1. تطبيق الرخصة:
 1. إذا كنت قد اشتريت ترخيصًا ، فاستخدم الترخيص الموجود في التطبيق الخاص بك للوصول إلى الوظائف الكاملة Aspose.Diagram
 1. إذا كنت تستخدم الإصدار التقييمي للمكون (إذا كنت تستخدم Aspose.Diagram بدون ترخيص) ، فتخط هذه الخطوة.
1. قم بتكوين ملف Microsoft Visio جديد ، أو افتح ملفًا موجودًا تريد إضافة / تحديث جزء منه.
1.  أدخل الكلمات**Hello World!** في الصفحة التي تم الوصول إليها.
1. قم بإنشاء ملف Microsoft Visio المعدل.

توضح الأمثلة أدناه الخطوات المذكورة أعلاه.

#### **إنشاء Diagram**

ينشئ المثال التالي diagram جديدًا من البداية ، ويكتب الكلمات "Hello World!" في الصفحة الأولى ، ويحفظ الملف.

**قم بإنشاء ملف visio جديد** 

![ما يجب القيام به: image_بديل_نص](your-first-aspose-diagram-application-hello-world_1.png)


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


#### **فتح ملف موجود**

يفتح المثال التالي ملف قالب Microsoft Visio موجود ، ويكتب الكلمات "Hello World!" في الصفحة الأولى ، ويحفظ diagram كملف جديد.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

diagram = Diagram(os.path.join(sourceDir, "Basic Shapes.vss"))

#// Add a new hello world rectangle shape
shapeId = diagram.add_shape(4.25, 5.5, 2, 1, "Rectangle", 0)
shape = diagram.pages[0].shapes.get_shape(shapeId)
shape.text.value.add(Txt("Hello World"))

#// Save diagram in the VSDX format
diagram.save("CreateHelloWorldVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}

