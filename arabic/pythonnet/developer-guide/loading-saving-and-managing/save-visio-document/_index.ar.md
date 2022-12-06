---
title: احفظ Visio الوثيقة برمجيا
linktitle: احفظ الوثيقة Visio
type: docs
weight: 30
url: /ar/python-net/save-visio-document/
description: تصف هذه الصفحة كيفية حفظ Visio مستند إلى ملف ، دفق باستخدام مكتبة Aspose.Diagram.
---
## **Visio نظرة عامة على حفظ الرسم**
 استخدم ال[Diagram.Save]() طريقة لحفظ رسم Microsoft Visio. هناك حمولات زائدة تسمح بحفظ رسم في ملف. يمكن حفظ الرسم بأي تنسيق حفظ يدعمه Aspose.Diagram. للحصول على قائمة بجميع تنسيقات الحفظ المدعومة ، راجع ملف[SaveFileFormat]() تعداد.
## **توفير Visio Diagram**
 تمثل الفئة Diagram من Aspose.Diagram API رسمًا Visio ويمكن للمطورين حفظ كائن Visio diagram بأي تنسيق ملف مدعوم. لحفظ ملف Microsoft Visio ، ما عليك سوى استخدام ملحق[Diagram.Save]()الأسلوب ، فإنه يقبل اسم ملف بمسار كامل أو كائن دفق ملف. يستنتج Aspose.Diagram API تنسيق الحفظ من امتداد الملف ويقدم أيضًا معامل SaveFileFormat إضافيًا لتحديد تنسيق ملف الإخراج.
### **احفظ Visio Diagram بأي تنسيق ملف مدعوم**
باستخدام Aspose.Diagram API ، يمكن للمطورين حفظ Visio diagram بأي تنسيق ملف مدعوم كما هو موضح أدناه:
**VSDX و VSDM و VSSX و VSSM و VSTX و VSTM و VDX و VSX و VTX و TIFF و PNG و BMP و EMF و JPEG و 07611531183 و EMF و 07611331183 و EMF و JPEG**
### **حفظ Diagram عينة البرمجة**
المثال أدناه يحفظ مستندًا إلى ملف.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **تحديد Visio خيارات الحفظ**
 هناك العديد[Diagram.Save]() الأسلوب الزائد الذي يقبل كائن SaveOptions. يجب أن يكون هذا كائنًا من فئة مشتقة من فئة SaveOptions. يحتوي كل تنسيق حفظ على فئة مقابلة تحتوي على خيارات الحفظ لتنسيق الحفظ هذا. على سبيل المثال ، هناك PdfSaveOptions لتنسيق حفظ SaveFileFormat.PDF.
### **Visio Diagram حفظ الخيارات**
توضح هذه الأمثلة كيفية:

- [استخدم Diagram حفظ الخيارات](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [استخدم PDF حفظ الخيارات](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [استخدم HTML حفظ الخيارات](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [استخدم خيارات حفظ الصورة](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [استخدم SVG حفظ الخيارات](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [استخدم SWF حفظ الخيارات](https://docs.aspose.com/diagram/python-net/save-visio-document/).
#### **استخدام Diagram حفظ الخيارات**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ المستند بتنسيق Visio.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseDiagramSaveOptions.py" >}}



#### **استخدام PDF حفظ الخيارات**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند بتنسيق PDF.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UsePdfSaveOptions.py" >}}



#### **استخدام HTML حفظ الخيارات**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند بتنسيق ملف HTML.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseHtmlSaveOptions.py" >}}



#### **استخدام خيارات حفظ الصورة**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند بتنسيق ملف الصورة.



{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseImageSaveOptions.py" >}}


استخدام SVG حفظ الخيارات

يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ المستند بتنسيق SVG.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseSvgSaveOptions.py" >}}

في بعض الأحيان ، يحتاج المطورون إلى حفظ الرسوم التخطيطية Visio أو تصديرها إلى تنسيقات ملفات مختلفة برمجيًا (مثل VDX و PDF و JPEG وما إلى ذلك).

### ` `**حفظ VSD الملف في تنسيقات أخرى باستخدام Aspose.Diagram ل Python via .NET**
باستخدام Aspose.Diagram ، لا يحتاج المطورون إلى Microsoft Office Visio في الجهاز ، ويمكنهم العمل بشكل مستقل عن Microsoft Office Automation.

توضح مقتطفات التعليمات البرمجية أدناه كيفية:

1. قم بتحميل diagram.
1. احفظ diagram إلى VSX و PDF و JPEG.
#### **حفظ VSD الملف مع Aspose.Diagram ل Python via .NET عينة البرمجة**
{{% alert color="primary" %}} 

استيراد كهدف
من الغرض .diagram استيراد *

{{% /alert %}} 

**مثال:**

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-SaveDiagramTo_VDX_PDF_JPEG_withAspose.py" >}}
