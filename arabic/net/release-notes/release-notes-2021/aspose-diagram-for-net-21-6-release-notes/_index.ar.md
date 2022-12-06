---
title: Aspose.Diagram for .NET 21.6 ملاحظات الإصدار
type: docs
weight: 7
url: /ar/net/aspose-diagram-for-net-21-6-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for .NET 21.6.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-52007|الأداء أثناء تهيئة كائن diagram|التعزيز|
|DIAGRAMNET-52008|الأداء أثناء تهيئة كائن diagram|التعزيز|
|DIAGRAMNET-52027|جودة الأشكال ليست جيدة في ملف SVG المُصدَّر|التعزيز|
|DIAGRAMNET-52033|حفظ الأشكال لمشكلة HTML|حشرة|
|DIAGRAMNET-52035|"غير مستثنى من eof." استثناء عند فتح ملف VSDX|حشرة|
|DIAGRAMNET-52041|فشل حفظ بعض الأشكال من ملف VSS|حشرة|
|DIAGRAMNET-52042|"المعامل غير صالحة." استثناء عند تحويل ملف VSD إلى HTML|حشرة|
|DIAGRAMNET-52043|"مرجع كائن لم يتم تعيين إلى مثيل كائن." استثناء عند حفظ الشكل من ملف VSSX|حشرة|

## **عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.
### **تمت إضافة EmfRenderSetting في SVGSaveOptions**
- الإعداد لعرض ملف تعريف Emf

{{< highlight "java" >}}

SVGSaveOptions o = new SVGSaveOptions();
o.EmfRenderSetting = Aspose.Diagram.EmfRenderSetting.EmfPlusPrefer;

{{< /highlight >}}
### **يضيف InheritTextBlock في الشكل**
- يحتوي على قيم كتلة النص للشكل الذي يرثه النمط الأصل والشكل الرئيسي.



{{< highlight "java" >}}

shape.InheritTextBlock

{{< /highlight >}}





