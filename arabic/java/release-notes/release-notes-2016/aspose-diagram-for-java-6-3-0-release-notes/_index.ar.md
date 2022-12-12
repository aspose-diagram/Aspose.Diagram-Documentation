﻿---
title: Aspose.Diagram for Java 6.3.0 ملاحظات الإصدار
type: docs
weight: 90
url: /ar/java/aspose-diagram-for-java-6-3-0-release-notes/
---
## **تحسينات وتغييرات أخرى**

|**مفتاح** |**ملخص** |**فئة** |
|:- |:- |:- |
| الرسم البياني جافا -50306| إضافة دعم للكشف عن نوع Visio diagram.| ميزة جديدة|
| الرسم البياني جافا -50311|منع تصدير الصفحات المخفية Visio في PDF.| ميزة جديدة|
| الرسم البياني جافا -50312|منع تصدير الصفحات المخفية Visio في HTML.| ميزة جديدة|
| الرسم البياني جافا -50313|منع تصدير الصفحات المخفية Visio في PNG.| ميزة جديدة|
| الرسم البياني جافا -50314|منع تصدير الصفحات المخفية Visio في JPEG.| ميزة جديدة|
|الرسم البياني جافا -50315|منع تصدير الصفحات المخفية Visio في SVG.| ميزة جديدة|
| الرسم البياني جافا -50316| منع تصدير الصفحات المخفية Visio في GIF.| ميزة جديدة|
| الرسم البياني جافا -50317|منع تصدير الصفحات المخفية Visio في XPS.| ميزة جديدة|
| الرسم البياني جافا -50307| يقوم VDX إلى VSDX بتعليم اختيار خط شبكة الصفحة محددًا.| حشرة|
| الرسم البياني جافا -50308| قم بفتح وحفظ الإجراء VSDX لتغيير النص إلى أحرف وهمية.| حشرة|
| الرسم البياني جافا -50309| أدى إجراء فتح وحفظ VSDX إلى تغيير شكل الخط المنقط.| حشرة|
| الرسم البياني جافا -50310| فتح وحفظ الإجراء VSDX يغير خط النص والخط الغامق.| حشرة|
| الرسم البياني جافا -50318| يؤدي تصدير VSD إلى VDX إلى ظهور خطأ العنصر الرئيسي.| حشرة|
### **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
راجع قائمة أي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفين أو المهملين بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه على[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
#### **قم بإضافة فئات FileFormatUtil و FileFormatInfo.**
تمنح هذه الفئات وصولاً برمجيًا لاكتشاف نوع الملف Visio.
#### **يضيف طريقة detectFileFormat في فئة FileFormatUtil.**
يقوم باكتشاف وإرجاع المعلومات حول تنسيق diagram Visio المخزن في ملف.
#### **إضافة خاصية FileFormatType في فئة FileFormatInfo**
يحصل على تنسيق الملف المكتشف.
#### **يضيف خاصية LoadFormat في FileFormatInfo**
يحصل على تنسيق التحميل المكتشف.
#### **يضيف setExportHiddenPage في SVGSaveOptions و XPSSaveOptions و ImageSaveOptions و HTMLSaveOptions و PdfSaveOptions**
وهي تحدد ما إذا كنت بحاجة إلى تصدير صفحات Visio المخفية أم لا.
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

- [التحكم في تصدير الصفحات المخفية Visio عند الحفظ]()
- [كشف تنسيق ملف Visio]()