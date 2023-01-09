---
title: Aspose.Diagram for .NET 18.9 ملاحظات الإصدار
type: docs
weight: 40
url: /ar/net/aspose-diagram-for-net-18-9-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 18.9](https://www.nuget.org/packages/Aspose.Diagram/18.9.0).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51509|VSDX إلى PNG - فقد عتامة الخط في صورة الإخراج|التعزيز|
|DIAGRAMNET-51510|VSDX إلى SVG - فقد عتامة الخط في صورة الإخراج|التعزيز|
|DIAGRAMNET-51516|دمج ملفات VISIO المتعددة في إخراج واحد|التعزيز|
|DIAGRAMNET-50272|VSD إلى SVG التحويل - بعض نقاط الاتصال لها موقع وحجم خاطئان|حشرة|
|DIAGRAMNET-50273|VSD إلى SVG - محاذاة عناصر نص الشكل غير صحيحة|حشرة|
|DIAGRAMNET-50487|VSD إلى HTML - تم وضع حرف الخط المائل بين القيمة في غير مكانه|حشرة|
|DIAGRAMNET-50975|VSDX إلى PDF - لون خلفية الشكل أسود|حشرة|
|DIAGRAMNET-50976|VSDX إلى HTML - لون خلفية الشكل أسود|حشرة|
|DIAGRAMNET-50980|VSDX إلى PNG - الأرقام الموجودة داخل الأشكال الماسية في غير محلها|حشرة|
|DIAGRAMNET-51129|لم تتم محاذاة عناصر النص بشكل صحيح عند تحويل VSD إلى PDF|حشرة|
|DIAGRAMNET-51511|رؤوس سهام إضافية في التحويل PNG|حشرة|
|DIAGRAMNET-51512|تظهر رؤوس سهام إضافية في تحويل SVG|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
#### **تمت إضافة طريقة الدمج في فئة Diagram**
يتم دمج Diagram مع عنصر Diagram آخر.

{{< highlight "java" >}}

             Diagram diagramF = new Diagram( "f.vsdx");

            Diagram diagramS = new Diagram( "s.vsdx");

            diagramF.Combine(diagramS);

{{< /highlight >}}
