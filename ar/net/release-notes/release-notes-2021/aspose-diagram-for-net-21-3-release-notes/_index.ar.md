---
title: Aspose.Diagram for .NET 21.3 ملاحظات الإصدار
type: docs
weight: 10
url: /ar/net/aspose-diagram-for-net-21-3-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for .NET 21.3.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51967|تصغير وطباعة Diagram على صفحة واحدة|التعزيز|
|DIAGRAMNET-51995|مشاكل متعلقة بملفات Aspose.Diagram و Skyline Dataminer|التعزيز|
|DIAGRAMNET-51996|طريقة CenterDrawing فيما يتعلق بالصفحة|التعزيز|
|DIAGRAMNET-52000|IsIntersect لا يعمل بشكل صحيح مع diagram|التعزيز|
|DIAGRAMNET-52003|ألصق الموصلات بالشكل باستخدام خلايا EndX و BeginX|التعزيز|
|DIAGRAMNET-51565|VSDX إلى PDF - الأشكال ونمط الخلفية مفقود|حشرة|
|DIAGRAMNET-51992|ينتج عن التصدير من vsdx إلى svg عرض غير صحيح في IE أو Chrome أو Firefox|حشرة|
|DIAGRAMNET-51997|فشل إعداد الترخيص باستثناء Aspose.Diagram عند استخدام ترخيص Aspose.Total لجميع واجهات برمجة التطبيقات في وظيفة Azure|حشرة|
|DIAGRAMNET-51998|سمة geoms للشكل عبارة عن قائمة فارغة في الإصدار> 20.3.0|حشرة|
|DIAGRAMNET-51999|تعذر تحديث العناصر الموروثة|حشرة|
|DIAGRAMNET-52004|تصدير VSDX كـ SVG بعض الحواف مفقودة|حشرة|
|DIAGRAMNET-52005|تحويل VSD إلى VSDX مشكلة|حشرة|
|DIAGRAMNET-52009|الأشكال مفقودة أثناء تحويل Visio إلى HTML|حشرة|

## ` `**عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
` ` فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على for .NET Aspose.Diagram. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه على منتدى الدعم Aspose.Diagram.
### **تمت إضافة ConnectShapesViaConnector في الصفحة**
- ربط الأشكال via موصل.

{{< highlight "java" >}}

diagram.Pages[pageNumber].ConnectShapesViaConnector(ampShape.ID, "Port7", wssShape.ID, "Port21", lineShape.ID);

{{< /highlight >}}
### **يضيف GlueShapeToConnectorBeginX في الصفحة**
- شكل الغراء باستخدام BeginX



{{< highlight "java" >}}

diagram.Pages[pageNumber].GlueShapeToConnectorBeginX(ampShape.ID, "Port7", lineShape.ID);

{{< /highlight >}}
### **يضيف GlueShapeToConnectorEndX في الصفحة**
- شكل الغراء باستخدام BeginX



{{< highlight "java" >}}

diagram.Pages[pageNumber].GlueShapeToConnectorEndX(wssShape.ID, "Port21", lineShape.ID);

{{< /highlight >}}
### **يضيف CenterDrawing في الصفحة**
- توسيط أشكال الصفحة فيما يتعلق بنطاق الصفحة.



{{< highlight "java" >}}

diagram.Pages[pageNumber].CenterDrawing();

{{< /highlight >}}
### **يضيف IsContain في الشكل**
- الإشارة إلى ما إذا كان هذا الشكل يحتوي على شكل آخر.



{{< highlight "java" >}}

OLE_Shape.IsContain(shape)

{{< /highlight >}}



