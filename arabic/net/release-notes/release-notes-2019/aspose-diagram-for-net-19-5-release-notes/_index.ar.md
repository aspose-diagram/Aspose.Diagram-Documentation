﻿---
title: Aspose.Diagram for .NET 19.5 ملاحظات الإصدار
type: docs
weight: 80
url: /ar/net/aspose-diagram-for-net-19-5-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 19.5](https://www.nuget.org/packages/Aspose.Diagram/19.5.0)

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51606|كشف وإزالة السمات غير المستخدمة ورسومات البيانات والأنماط من Visio الرسوم البيانية|التعزيز|
|DIAGRAMNET-51637|لا يتم الاحتفاظ بالشكل المتداخل داخل حاوية مجمعة بشكل صحيح|التعزيز|
|DIAGRAMNET-51638|تعذر الحصول على Prop.Value.Val عندما تكون القيمة عددًا صحيحًا|التعزيز|
|DIAGRAMNET-51640|تحديد الأنماط غير المستخدمة في ملف Visio|التعزيز|
|DIAGRAMNET-50051|VSDX إلى PDF التحويل ، سهم الاتصال مفقود مع النص في غير مكانه|حشرة|
|DIAGRAMNET-50052|VSDX إلى PDF التحويل ، الأشكال ذات لون الخط غير الصحيح|حشرة|
|DIAGRAMNET-51179|تظليل غير صحيح فوق زر بريد إلكتروني عند تحويل VSDM إلى SVG|حشرة|
|DIAGRAMNET-51190|عرض غير صحيح للشكل المرتبط تشعبيًا عند حفظ VDX إلى SVG|حشرة|
|DIAGRAMNET-51194|عرض غير صحيح لرمز عند حفظ VDX إلى SVG|حشرة|
|DIAGRAMNET-51254|تظليل غير صحيح في الشريط العلوي عند تحويل VSDM إلى SVG|حشرة|
|DIAGRAMNET-51618|Visio إلى PDF - تنسيق تاريخ غير صحيح وبيانات مفقودة|حشرة|
|DIAGRAMNET-51628|قيمة نصية غير صحيحة للنص الافتراضي المحذوف في الرسوم التخطيطية .vsdx|حشرة|
|DIAGRAMNET-51634|Visio إلى SVG - فهرس z خاطئ لبعض الأشكال في الإخراج|حشرة|
|DIAGRAMNET-51636|Visio إلى SVG - لم يتم تصدير كل عناصر المسار بشكل صحيح كعناصر مستقيمة|حشرة|
|DIAGRAMNET-51641|تظهر الصورة الإضافية عند إعادة حفظ Visio بـ API|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف GetUnusedStyles في Diagram**
احصل على أنماط غير مستخدمة.

{{< highlight "java" >}}

  StyleSheetCollection unused = diagram.GetUnusedStyles();

{{< /highlight >}}