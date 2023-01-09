---
title: Aspose.Diagram for .NET 21.12 ملاحظات الإصدار
type: docs
weight: 1
url: /ar/net/aspose-diagram-for-net-21-12-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for .NET 21.12.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-52408|المشكلات التي تحدث عند استخدام EmfRederSetting EmfPlusPrefer|التعزيز|
|DIAGRAMNET-52438|SaveForegroundPagesOnly للطباعة|التعزيز|
|DIAGRAMNET-52450|Visio إلى SVG - حفظ الصورة النقطية بشكل منفصل|التعزيز|
|DIAGRAMNET-51171|عرض جزئي للأشكال عند حفظ الرسم بتنسيق PDF|حشرة|
|DIAGRAMNET-51390|لم يتم استبدال الكائن المضمن بشكل صحيح|حشرة|
|DIAGRAMNET-51800|Visio إلى SVG - صورة الخلفية مفقودة (تمت إضافة PowerPoint في VISIO)|حشرة|
|DIAGRAMNET-52423|Page.Copy () لا ينسخ كائن Excel في diagram|حشرة|
|DIAGRAMNET-52443|الأشكال مفقودة أثناء فتح وحفظ MS Visio Diagram|حشرة|
|DIAGRAMNET-52444|Visio إلى JPG - نتائج مختلفة تم إنشاؤها بواسطة API|حشرة|
|DIAGRAMNET-52445|تحويل العينة على بيئة Linux و Windows لهما نتيجة مختلفة|حشرة|

## **عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.


### **يضيف IsSavingImageSeparately في SVGSaveOptions**
- يحدد ما إذا كان يتم حفظ الصورة بشكل منفصل.

{{< highlight "java" >}}

    SVGSaveOptions o = new SVGSaveOptions();
    o.IsSavingImageSeparately = true;

{{< /highlight >}}


### **يضيف CustomImagePath في SVGSaveOptions**
- المسار المخصص للمستخدم (URL) المحفوظ في ملف svg الذي تم إنشاؤه للصورة. إذا لم يتم تحديده من قبل المستخدم ، فسيتم استخدام الدليل الحالي.

{{< highlight "java" >}}

  o.CustomImagePath = "d:/output/";

{{< /highlight >}}

### **يضيف SaveForegroundPagesOnly في PrintSaveOptions**
- يحدد ما إذا كانت جميع الصفحات ستتم طباعتها أم في المقدمة فقط.

{{< highlight "java" >}}

 PrintSaveOptions options = new PrintSaveOptions();
 options.SaveForegroundPagesOnly = true;

{{< /highlight >}}
