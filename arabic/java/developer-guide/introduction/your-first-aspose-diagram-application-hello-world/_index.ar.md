---
title: أول تطبيق Aspose.Diagram لك - أهلاً بالعالم
type: docs
weight: 30
url: /ar/java/your-first-aspose-diagram-application-hello-world/
description: توضح هذه الصفحة كيفية إنشاء التطبيق الأول باستخدام مكتبة Aspose.Diagram.
---
{{% alert color="primary" %}}

يوضح هذا البرنامج التعليمي كيفية إنشاء أول تطبيق (Hello World) باستخدام Aspose.Diagram 'simple API. هذا التطبيق البسيط يقوم بإنشاء ملف Microsoft Visio مع النص "Hello World" في صفحة محددة.

{{% /alert %}}

## **إنشاء تطبيق Hello World**

الخطوات التالية تنشئ تطبيق Hello World باستخدام Aspose.Diagram API:

1.  قم بإنشاء مثيل لـ[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) صف دراسي.
1.  إذا كان لديك ترخيص ، إذن[قم بتطبيقه](https://reference.aspose.com/diagram/java/com.aspose.diagram/License).
 إذا كنت تستخدم الإصدار التقييمي ، فتخط سطور التعليمات البرمجية المتعلقة بالترخيص.
1. قم بتكوين ملف Visio جديد ، أو افتح ملف Visio موجود.
1. قم بإنشاء مربع نص جديد.
1.  أدخل الكلمات**مرحبا بالعالم!** في مربع نص.
1. قم بإنشاء ملف Microsoft Visio المعدل.

يتم توضيح تنفيذ الخطوات المذكورة أعلاه في الأمثلة أدناه.

### **نموذج التعليمات البرمجية: إنشاء Diagram جديد**

المثال التالي ينشئ diagram جديدًا من البداية ، يكتب Hello World! في الصفحة الأولى ويحفظ الملف Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-CreateNewVisio-CreateNewVisio.java" >}}

### **نموذج التعليمات البرمجية: فتح ملف موجود**

يفتح المثال التالي ملف قالب Microsoft Visio موجود باسم "Sample.vsdx" ، بإدخال "Hello World!" نص في الصفحة الأولى ويحفظ diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ReadVisioDiagram-ReadVisioDiagram.java" >}}
