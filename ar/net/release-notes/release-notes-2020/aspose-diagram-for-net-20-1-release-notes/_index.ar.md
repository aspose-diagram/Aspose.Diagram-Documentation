---
title: Aspose.Diagram for .NET 20.1 ملاحظات الإصدار
type: docs
weight: 70
url: /ar/net/aspose-diagram-for-net-20-1-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for .NET 20.1.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51198|لم يتم تقديم التظليل الموجود على زر الارتباط التشعبي بشكل صحيح عند حفظ VSDM إلى SVG|التعزيز|
|DIAGRAMNET-51526|VSDX إلى PDF - فقدان التعبئة المتدرجة لرؤوس الأسهم نتيجة PDF|التعزيز|
|DIAGRAMNET-51539|فقد التدرج اللوني في الأشكال في الإخراج SVG|التعزيز|
|DIAGRAMNET-50705|تصدير VSD إلى SVG - تتحول أشكال نوع Meta إلى رموز فوضوية|حشرة|
|DIAGRAMNET-51664|تلف الملف بعد إزالة المظهر غير المستخدم|حشرة|
|DIAGRAMNET-51665|يتم عرض الصور على أنها X بعد إزالة السمات غير المستخدمة|حشرة|
|DIAGRAMNET-51684|أثناء إزالة الأشكال والأنماط الرئيسية غير المستخدمة ، توجد مشكلة في الصورة فقط|حشرة|
|DIAGRAMNET-51726|فقدان صورة الخلفية (تمت إضافة PowerPoint في VISIO) أثناء إزالة الأشكال والأنماط الرئيسية غير المستخدمة|حشرة|
|DIAGRAMNET-51737|Visio إلى Html - مشكلة حجم الصورة|حشرة|
|DIAGRAMNET-51743|إزالة المعلومات الخاصة من Visio - مشكلة حجم المستند Visio|حشرة|
|DIAGRAMNET-51745|يحدث خطأ غريب في تطبيق WPF عند تحويل VSD إلى VSDX|حشرة|

## **عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
- الصفحات المضافة إلى LoadOptions - يحدد فهرس الصفحات المراد تحميلها.



{{< highlight "java" >}}

Aspose.Diagram.LoadOptions options = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);

options.Pages = new ArrayList();

options.Pages.Add(0);

{{< /highlight >}}

- تمت إضافة SetFontSources في FontConfigs - لتعيين مصادر الخطوط

{{< highlight "java" >}}

Aspose.Diagram.MemoryFontSource sc1 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource sc2 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource[]sc = new Aspose.Diagram.MemoryFontSource[]{ sc1, sc2 };

Aspose.Diagram.FontConfigs.SetFontSources(sc); 

{{< /highlight >}}
