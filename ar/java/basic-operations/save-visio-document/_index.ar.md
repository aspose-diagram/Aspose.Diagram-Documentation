---
title: احفظ Visio الوثيقة برمجيا
linktitle: احفظ الوثيقة Visio
type: docs
weight: 30
url: /ar/java/save-visio-document/
description: تصف هذه الصفحة كيفية حفظ Visio مستند إلى ملف ، دفق باستخدام مكتبة Aspose.Diagram.
---
## **Visio نظرة عامة على حفظ الرسم**
 استخدم ال[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\) طريقة لحفظ Microsoft Visio رسم. هناك حمولات زائدة تسمح بحفظ رسم في ملف. يمكن حفظ الرسم بأي تنسيق حفظ يدعمه Aspose.Diagram. للحصول على قائمة بجميع تنسيقات الحفظ المدعومة ، راجع ملف[SaveFileFormat](https://reference.aspose.com/diagram/java/com.aspose.diagram/SaveFileFormat) تعداد.
## **توفير Visio Diagram**
 تمثل الفئة Diagram من Aspose.Diagram API رسمًا Visio ويمكن للمطورين حفظ كائن Visio diagram بأي تنسيق ملف مدعوم. لحفظ ملف Microsoft Visio ، ما عليك سوى استخدام ملحق[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) ، فهو يقبل اسم ملف بالمسار الكامل أو كائن دفق الملف. يستنتج Aspose.Diagram API تنسيق الحفظ من امتداد الملف ويقدم أيضًا معامل SaveFileFormat إضافيًا لتحديد تنسيق ملف الإخراج.
### **احفظ Visio Diagram بأي تنسيق ملف مدعوم**
باستخدام Aspose.Diagram API ، يمكن للمطورين حفظ Visio diagram بأي تنسيق ملف مدعوم كما هو موضح أدناه:
**VSDX ، VSDM ، VSSX ، VSSM ، VSTX ، VSTM ، VDX ، VSX ، VTX ، TIFF ، PNG ، BMP ، EMF ، 07611331183 ، EMF ، JPEG ، 07611531183 ، EMF ، JPEG ، JPEG ، EMF ، JPEG ، EMF**
### **حفظ Diagram عينة البرمجة**
المثال أدناه يحفظ مستندًا إلى ملف.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-SaveVisioDiagram-SaveVisioDiagram.java" >}}
## **تحديد Visio خيارات الحفظ**
 هناك العديد[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)طريقة overloads التي تقبل كائن SaveOptions. يجب أن يكون هذا كائنًا من فئة مشتقة من فئة SaveOptions. يحتوي كل تنسيق حفظ على فئة مقابلة تحتوي على خيارات الحفظ لتنسيق الحفظ هذا ، على سبيل المثال ، هناك PdfSaveOptions لتنسيق SaveFileFormat.PDF.
### **Visio Diagram حفظ الخيارات**
توضح هذه الأمثلة كيفية:

- [استخدم Diagram حفظ الخيارات](/diagram/ar/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [استخدم PDF حفظ الخيارات](/diagram/ar/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [استخدم HTML حفظ الخيارات](/diagram/ar/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [استخدم خيارات حفظ الصورة](/diagram/ar/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [استخدم SVG حفظ الخيارات](/diagram/ar/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
#### **استخدام Diagram حفظ الخيارات**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ المستند بتنسيق Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.java" >}}



#### **استخدام PDF حفظ الخيارات**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند بتنسيق PDF.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.java" >}}



#### **استخدام HTML حفظ الخيارات**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند بتنسيق HTML.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.java" >}}



#### **استخدام خيارات حفظ الصورة**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند إلى تنسيق صورة.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.java" >}}
#### **استخدام SVG حفظ الخيارات**
يوضح الكود أدناه كيفية تعيين خيارات الحفظ قبل حفظ المستند بتنسيق SVG.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.java" >}}
