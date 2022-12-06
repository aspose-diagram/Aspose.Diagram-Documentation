---
title: API العام التغييرات في Aspose.Diagram 6.3.0
type: docs
weight: 40
url: /ar/java/public-api-changes-in-aspose-diagram-6-3-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 6.0.0 إلى 6.3.0 ، والتي قد تهم مطوري الوحدة النمطية / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
## **كشف تنسيق ملف Visio**
### **تمت إضافة فئات وطرق وخصائص مختلفة لاكتشاف التنسيق**
- **قم بإضافة فئات FileFormatUtil و FileFormatInfo** 
 - تمنح هذه الفئات وصولاً برمجيًا لاكتشاف نوع الملف Visio.
- **يضيف طريقة detectFileFormat في فئة FileFormatUtil** 
 - يكتشف ويعيد المعلومات الخاصة بتنسيق diagram Visio المخزن في ملف.
- **إضافة خاصية FileFormatType في فئة FileFormatInfo** 
 - يحصل على تنسيق الملف المكتشف.
- **يضيف خاصية LoadFormat في FileFormatInfo** 
 - يحصل على تنسيق التحميل المكتشف.

 يمكن للمطورين اكتشاف تنسيق أي ملف Visio بسهولة. يوضح موضوع التعليمات هذا كيفية اكتشاف تنسيق ملف Visio (باستخدام مسار ملف أو دفق) والتحقق من امتداده:[كشف تنسيق ملف Visio](/diagram/ar/java/introduction/#Introduction-DetecttheFormatofVisioFile)
## **التحكم في تصدير الصفحات المخفية Visio عند الحفظ**
### **يضيف setExportHiddenPage في فئات SVGSaveOptions و XPSSaveOptions و ImageSaveOptions و HTMLSaveOptions و PdfSaveOptions Classes**
- وهي تحدد ما إذا كنت بحاجة إلى تصدير صفحات Visio المخفية أم لا.

 قد يقوم المطورون بتضمين أو استبعاد صفحات Visio المخفية عند حفظ Visio diagram إلى ملفات PDF و HTML و Image (PNG و JPEG و GIF) و SVG و XPS. يوضح موضوع التعليمات هذا كيفية القيام بذلك:[التحكم في تصدير الصفحات المخفية Visio عند الحفظ](/diagram/ar/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
