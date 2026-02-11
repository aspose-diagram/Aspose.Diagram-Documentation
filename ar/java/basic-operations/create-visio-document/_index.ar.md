---
title: تكوين وثيقة Visio برمجيا
linktitle: تكوين وثيقة Visio
type: docs
weight: 10
url: /ar/java/create-visio-document/
description: توضح هذه الصفحة كيفية إنشاء مستند Visio من البداية باستخدام مكتبة Aspose.Diagram.
---
## **تكوين رسم Visio جديد**
يتيح لك Aspose.Diagram for Java قراءة وإنشاء Microsoft Visio الرسوم التخطيطية من داخل التطبيقات الخاصة بك ، بدون أتمتة Microsoft Office. الخطوة الأولى عند إنشاء مستندات جديدة ، هي إنشاء diagram. ثم إضافة الأشكال والموصلات لبناء diagram.
### **إنشاء Visio نموذج لبرمجة الرسم**
يظهر الكود أدناه لإنشاء رسم Microsoft Visio جديد. يرجى ملاحظة أن الرسم الفارغ يحتوي على صفحة فارغة واحدة.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}} 

حجم ورق الرسم هو Letter بشكل افتراضي.

{{% /alert %}} 

