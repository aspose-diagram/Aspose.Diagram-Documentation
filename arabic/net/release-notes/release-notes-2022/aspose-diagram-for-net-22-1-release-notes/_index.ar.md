---
title: Aspose.Diagram for .NET 22.1 ملاحظات الإصدار
type: docs
weight: 27
url: /ar/net/aspose-diagram-for-net-22-1-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار لـ Aspose.Diagram for .NET 22.1.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-50560|دعم حفظ المخططات إلى HTML مع أو بدون موارد مضمنة|التعزيز|
|DIAGRAMNET-52499|إضافة دعم لحفظ لغة تأشير النص الفائق إلى دفق واحد|التعزيز|
|DIAGRAMNET-50562|VSDX إلى PDF - الأشكال مفقودة من الإخراج|حشرة|
|DIAGRAMNET-50780|لا تظهر خطوط حدود الجداول عند حفظ VSDX في PDF|حشرة|
|DIAGRAMNET-50962|خطوط حدود الجداول مفقودة عند تحويل VSDX إلى PNG|حشرة|
|DIAGRAMNET-50992|لا يظهر خط الحد الأيسر للجدول عند تحويل VSDX إلى PDF|حشرة|
|DIAGRAMNET-51034|تظليل الأشكال مفقود عند تحويل VSDX إلى PDF|حشرة|
|DIAGRAMNET-51186|تخطيط غير صحيح لأشكال نوع التعريف عند تحويل VSD إلى PDF|حشرة|
|DIAGRAMNET-51226|Aspose.Diagram 17.3.0: الحفظ في تدفق HTML لا يقوم بتضمين المصادر الخارجية|حشرة|
|DIAGRAMNET-52506|Page.Copy () لا ينسخ تغييرات المطور|حشرة|

## **عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.


### **يضيف SaveAsSingleFile في HTMLSaveOptions**
- يشير إلى ما إذا كنت ستحفظ html كملف فردي.

{{< highlight "java" >}}

    HTMLSaveOptions ho = new HTMLSaveOptions();
    ho.SaveAsSingleFile = true;

{{< /highlight >}}