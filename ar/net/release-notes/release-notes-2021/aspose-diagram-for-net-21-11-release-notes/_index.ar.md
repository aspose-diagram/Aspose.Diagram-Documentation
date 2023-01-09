---
title: Aspose.Diagram for .NET 21.11 ملاحظات الإصدار
type: docs
weight: 2
url: /ar/net/aspose-diagram-for-net-21-11-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for .NET 21.11.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51111|التعبئة المتدرجة للدوائر خطأ عند تحويل VDX إلى EMF|التعزيز|
|DIAGRAMNET-52377|إضافة دعم تحميل vsd بالإصدار القديم 3|التعزيز|
|DIAGRAMNET-51364|VSDX إلى PNG - فقد نص عنصر OLE المضمن|حشرة|
|DIAGRAMNET-52329|VSDX إلى HTML - الرموز التعبيرية غير موجودة في الإخراج|حشرة|
|DIAGRAMNET-52345|يتم فقد "تذييل الرأس" بعد حفظ الملف Diagram|حشرة|
|DIAGRAMNET-52349|Visio إلى HTML - تم قطع الحواف اليمنى واليسرى|حشرة|
|DIAGRAMNET-52374|ArgumentOutOfRangeException أثناء الحفظ في PDF|حشرة|
|DIAGRAMNET-52386|لماذا يمكن تكرار بعض الصفحات diagram والبعض الآخر لا يمكنه استخدام Page.Copy ()؟|حشرة|

## **عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.


### **يضيف PresetTheme في الشكل**
- قم بتطبيق نسق محدد مسبقًا على هذا الشكل.

{{< highlight "java" >}}

shape.PresetTheme = PresetThemeValue.Bubble;

{{< /highlight >}}


### **يضيف PresetThemeVariant في الشكل**
- قم بتطبيق متغير نسق محدد مسبقًا على هذا الشكل

{{< highlight "java" >}}

shape.PresetThemeVariant = PresetThemeVariantValue.Variant1;

{{< /highlight >}}

### **يضيف PresetThemeQuickStyle في الشكل**
- قم بتطبيق نمط سريع متغير للنسق مُعد مسبقًا على هذا الشكل

{{< highlight "java" >}}

 shape.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle1;

{{< /highlight >}}
