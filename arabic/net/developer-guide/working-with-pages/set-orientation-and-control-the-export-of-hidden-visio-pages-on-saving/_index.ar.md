---
title: قم بتعيين الاتجاه والتحكم في تصدير صفحات Visio المخفية عند الحفظ
type: docs
weight: 20
url: /ar/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
description: يوضح هذا القسم كيفية تعيين تخطيط الصفحة باستخدام Aspose.Diagram.
---
## **قم بتغيير نسق الصفحة Visio إلى عمودي أو أفقي**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) يسمح API للمطورين بتعيين اتجاه صفحة الرسم Visio برمجيًا. يشرح موضوع التعليمات هذا كيفية إنجاز هذه المهمة.

 Aspose.Diagram for .NET API لديه[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) فئة تمثل Visio صفحة رسم. تعرض الخاصية PageSheet بواسطة فئة الصفحة أيضًا خصائص الطباعة. يسمح حقل PrintPageOrientation لخصائص الطباعة بتدوير الصفحة. يوفر ثلاثة خيارات مثل عمودي وأفقي ونفس الشيء كما هو الحال في الطابعة. يمكن تعيين حقل PrintPageOrientation برمجيًا باستخدام Aspose.Diagram API.

هذا المثال يعمل على النحو التالي:

1. قم بتحميل Visio diagram موجود في كائن الفئة Diagram.
1. قم باستخراج صفحة Visio
1. عيّن اتجاهه على أنه عمودي أو أفقي أو نفس الاتجاه على الطابعة.
1. احفظ Visio diagram.
### **تعيين عينة برمجة الاتجاه**
يوضح مثال الكود أدناه كيفية ضبط اتجاه الصفحة Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-SetVisioPageOrientation-SetVisioPageOrientation.cs" >}}
## **التحكم في تصدير الصفحات المخفية Visio عند الحفظ**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API يسمح للمطورين بتضمين أو استبعاد الصفحات المخفية Visio عند حفظ diagram إلى ملفات PDF و HTML و Image (PNG و JPEG و GIF) و SVG و XPS. حتى أنها قد تخفي Visio صفحات باستخدام Aspose.Diagram API لأن خيارها متاح بالفعل من خلال الخلية UIVisibility في صفحة ShapeSheet.
### **إخفاء صفحة في Visio Diagram وضبط خيار التصدير**
 Aspose.Diagram for .NET API لديه[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) فئة تمثل Visio صفحة رسم. تعرض خاصية PageSheet التي تم كشفها بواسطة فئة الصفحة أيضًا خصائص الصفحة. يسمح حقل UIVisibility الخاص بخصائص الصفحة بإخفاء الصفحة. يمكن للمطورين بعد ذلك استخدام خاصية ExportHiddenPage التي تمت إضافتها في فئات SVGSaveOptions و XPSSaveOptions و ImageSaveOptions و HTMLSaveOptions و PdfSaveOptions.
#### **اضبط خيار التصدير لملف PDF**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ diagram إلى تنسيق PDF.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToPDF-ExportOfHiddenVisioPagesToPDF.cs" >}}
#### **قم بتعيين خيار التصدير لـ HTML**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ diagram إلى تنسيق HTML.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToHTML-ExportOfHiddenVisioPagesToHTML.cs" >}}
#### **اضبط خيار التصدير للصورة**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ diagram إلى تنسيق الصورة.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.cs" >}}
#### **اضبط خيار التصدير لـ SVG**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ diagram بتنسيق SVG.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.cs" >}}
#### **قم بتعيين خيار التصدير لـ XPS**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ diagram بتنسيق XPS.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToXPS-ExportOfHiddenVisioPagesToXPS.cs" >}}
