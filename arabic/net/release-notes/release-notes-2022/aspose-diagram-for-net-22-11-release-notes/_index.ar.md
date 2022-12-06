---
title: Aspose.Diagram for .NET 22.11 ملاحظات الإصدار
type: docs
weight: 17
url: /ar/net/aspose-diagram-for-net-22-11-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for .NET 22.11.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-53011|أضف دعمًا لحفظ xaml كتدفق|التعزيز|
|DIAGRAMNET-53012|الصيغة لا مجال منعش|التعزيز|
|DIAGRAMNET-53024|الصيغة لا مجال منعش|التعزيز|
|DIAGRAMNET-53009|محادثة من vsdx إلى svg lost image|التعزيز|
|DIAGRAMNET-53010|التطبيق: حفظ vsdx إلى Pdf الأشكال المفقودة|حشرة|
|DIAGRAMNET-53013|Visio إلى SVG - نماذج الخط المخصصة|حشرة|
|DIAGRAMNET-53017|تم تغيير المنطقة المرتبطة في HTML من VSD إلى الإصدار 22.10.0.0|حشرة|
|DIAGRAMNET-53018|علة مع Paras.SpLine|حشرة|
|DIAGRAMNET-53019|يتم رسم خط إضافي في أسفل اليسار|حشرة|
|DIAGRAMNET-53033|لم يتم حساب قيم الخلايا بشكل صحيح|حشرة|
|DIAGRAMNET-53034|التغيير في شكل PinX يؤدي إلى تغيير الارتفاع|حشرة|

## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.

### **يضيف GetConnectorRule في الشكل**
- إرجاع قاعدة موصل تحتوي على معرف الشكل والموصل المتصلين بالشكل

{{< highlight "java" >}}
ConnectorRule rule= shape.GetConnectorRule();
{{< /highlight >}}

### **يضيف IsSavingCustomLinePattern في SVGSaveOptions**
- يحدد ما إذا كان يتم حفظ نمط الخط المخصص.

{{< highlight "java" >}}
var opt = new SVGSaveOptions()
{
     IsSavingCustomLinePattern = false
};
{{< /highlight >}}

### **يضيف StreamProvider في XAMLSaveOptions**
- الحصول على أو تعيين IStreamProvider لتصدير الكائنات

{{< highlight "java" >}}
MemoryStream stream = new MemoryStream();
var saveOptions = new XAMLSaveOptions();
var streamProvider = new XamlExportStreamProvider(".vsdx");
saveOptions.StreamProvider = streamProvider;
diagram.Save(stream, saveOptions);
{{< /highlight >}}