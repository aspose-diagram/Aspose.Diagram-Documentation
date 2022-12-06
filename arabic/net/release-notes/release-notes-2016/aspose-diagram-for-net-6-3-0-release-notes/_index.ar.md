---
title: Aspose.Diagram for .NET 6.3.0 ملاحظات الإصدار
type: docs
weight: 90
url: /ar/net/aspose-diagram-for-net-6-3-0-release-notes/
---
## **تحسينات وتغييرات أخرى**

|**مفتاح** |**ملخص** |**فئة** |
|:- |:- |:- |
|DIAGRAMNET-50739 | إضافة دعم للكشف عن نوع Visio diagram.| ميزة جديدة|
|DIAGRAMNET-50746 | منع تصدير الصفحات المخفية Visio في PDF.| ميزة جديدة|
|DIAGRAMNET-50747 | منع تصدير الصفحات المخفية Visio في HTML.| ميزة جديدة|
|DIAGRAMNET-50750 | منع تصدير الصفحات المخفية Visio في PNG.| ميزة جديدة|
|DIAGRAMNET-50751 | منع تصدير الصفحات المخفية Visio بتنسيق JPEG.| ميزة جديدة|
|DIAGRAMNET-50752 | منع تصدير الصفحات المخفية Visio في SVG.| ميزة جديدة|
|DIAGRAMNET-50753 | منع تصدير الصفحات المخفية Visio في GIF.| ميزة جديدة|
|DIAGRAMNET-50754 | منع تصدير الصفحات المخفية Visio في XPS.| ميزة جديدة|
|DIAGRAMNET-50541 | VSDX لتحويل PDF ، يتم عرض عناصر النص العبري بترتيب عكسي.| التعزيز|
|DIAGRAMNET-50542 | VSD لتحويل PDF ، تتحول الكلمة العربية إلى أحرف.| التعزيز|
|DIAGRAMNET-50682 | VSD للتصدير إلى PDF ، نص خلية الجدول غير مرئي جزئيًا.| حشرة|
|DIAGRAMNET-50712 | VDX إلى تصدير PDF - يتم وضع نص الأشكال المختلفة في غير محله.| حشرة|
|DIAGRAMNET-50741 | يفتقد VSD إلى تصدير SVG بعض أشكال Visio.| حشرة|
|DIAGRAMNET-50742 | VSD لتصدير SVG لا يطبق اللون الأبيض الداخلي للأشكال.| حشرة|
|DIAGRAMNET-50744 |تم تغيير إجراء فتح وحفظ VSDX النص إلى أحرف وهمية.| حشرة|
|DIAGRAMNET-50745 | أدى إجراء فتح وحفظ VSDX إلى تغيير شكل الخط المنقط.| حشرة|
|DIAGRAMNET-50748 | VSD إلى تصدير PDF - تم وضع عناصر النص في غير مكانها.| حشرة|
|DIAGRAMNET-50763 | يؤدي تصدير VSD إلى VDX إلى ظهور خطأ العنصر الرئيسي.| حشرة|
### **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
راجع قائمة أي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفين أو المهملين بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه على[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
#### **قم بإضافة فئات FileFormatUtil و FileFormatInfo**
تمنح هذه الفئات وصولاً برمجيًا لاكتشاف نوع الملف Visio.
#### **يضيف أسلوب DetectFileFormat في فئة FileFormatUtil**
يقوم باكتشاف وإرجاع المعلومات حول تنسيق diagram Visio المخزن في ملف.
#### **إضافة خاصية FileFormatType في فئة FileFormatInfo**
يحصل على تنسيق الملف المكتشف.
#### **يضيف خاصية LoadFormat في FileFormatInfo**
يحصل على تنسيق التحميل المكتشف.
#### **يضيف خاصية ExportHiddenPage في فئات SVGSaveOptions و XPSSaveOptions و ImageSaveOptions و HTMLSaveOptions و PdfSaveOptions Classes**
وهي تحدد ما إذا كنت بحاجة إلى تصدير صفحات Visio المخفية أم لا.
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

- [التحكم في تصدير الصفحات المخفية Visio عند الحفظ](/diagram/ar/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
- [كشف تنسيق ملف Visio](/diagram/ar/net/introduction/#detect-the-format-of-visio-file)
