---
title: قم بتعيين الاتجاه والتحكم في تصدير صفحات Visio المخفية عند الحفظ
type: docs
weight: 20
url: /ar/python-java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **قم بتغيير نسق الصفحة Visio إلى عمودي أو أفقي**
Aspose.Diagram لـ Python عبر Java API يسمح للمطورين بتعيين اتجاه صفحة الرسم Visio برمجيًا. يشرح موضوع التعليمات هذا كيفية إنجاز هذه المهمة.

Aspose.Diagram لـ Python عبر Java API به فئة `Page` التي تمثل Visio صفحة رسم. تعرض الخاصية PageSheet بواسطة فئة الصفحة أيضًا خصائص الطباعة. يسمح المجال `PrintPageOrientation` لخصائص الطباعة بتدوير الصفحة. يوفر ثلاثة خيارات مثل عمودي وأفقي ونفس الشيء كما هو الحال في الطابعة. يمكن تعيين حقل PrintPageOrientation برمجيًا باستخدام Aspose.Diagram لـ Python عبر Java API.

هذا المثال يعمل على النحو التالي:

1. قم بتحميل Visio diagram موجود في كائن الفئة Diagram.
1. قم باستخراج صفحة Visio
1. عيّن اتجاهه على أنه عمودي أو أفقي أو نفس الاتجاه على الطابعة.
1. احفظ Visio diagram.

### **تعيين عينة برمجة الاتجاه**
يوضح مثال الكود أدناه كيفية ضبط اتجاه الصفحة Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-SetVisioPageOrientation.py" >}}

## **التحكم في تصدير الصفحات المخفية Visio عند الحفظ**
Aspose.Diagram لـ Python عبر Java API يسمح للمطورين بتضمين أو استبعاد صفحات Visio المخفية عند حفظ diagram إلى ملفات PDF و HTML و Image (PNG و JPEG و GIF) و SVG و XPS. حتى أنها قد تخفي Visio صفحات باستخدام Aspose.Diagram لـ Python عبر Java API لأن خيارها متاح بالفعل من خلال الخلية UIVisibility في الصفحة ShapeSheet.

### **إخفاء صفحة في Visio Diagram وضبط خيار التصدير**
Aspose.Diagram لـ Python عبر Java API به فئة `Page` التي تمثل Visio صفحة رسم. تعرض خاصية PageSheet التي تم كشفها بواسطة فئة الصفحة أيضًا خصائص الصفحة. يسمح المجال `UIVisibility` لخصائص الصفحة بإخفاء الصفحة. يمكن للمطورين بعد ذلك استخدام خاصية `exportHiddenPage` التي تمت إضافتها في فئات `SVGSaveOptions` و `XPSSaveOptions` و `ImageSaveOptions` و `HTMLSaveOptions` و `PdfSaveOptions`.

#### **اضبط خيار التصدير لملف PDF**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ diagram إلى تنسيق PDF.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExporToHiddenVisioPagesToPdf.py" >}}

#### **قم بتعيين خيار التصدير لـ HTML**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ diagram إلى تنسيق HTML.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToHtml.py" >}}

#### **اضبط خيار التصدير للصورة**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ diagram إلى تنسيق الصورة.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToImage.py" >}}

#### **اضبط خيار التصدير لـ SVG**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ diagram بتنسيق SVG.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-ExportOfHiddenVisioPagesToSVG.py" >}}
