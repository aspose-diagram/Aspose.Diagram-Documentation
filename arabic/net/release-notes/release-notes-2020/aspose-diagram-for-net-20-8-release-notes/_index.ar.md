---
title: Aspose.Diagram for .NET 20.8 ملاحظات الإصدار
type: docs
weight: 14
url: /ar/net/aspose-diagram-for-net-20-8-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for .NET 20.8.

{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51886|إنشاء القدرة على إدراج كائن Ole مثل الكلمات والخلايا والشرائح وما إلى ذلك إلى Diagram في الشكل الفردي مع بيانات الكائن ومعاينة الصورة بداخله.|التعزيز|
|DIAGRAMNET-51888|Visio إلى PDF - يستغرق API وقتًا طويلاً للتحويل|التعزيز|
|DIAGRAMNET-51889|حفظ إلى pdf حلقات أكثر من 20 دقيقة|التعزيز|
|DIAGRAMNET-51893|سمة viewBox مفقودة بعد VSDX لتحويل SVG|التعزيز|
|DIAGRAMNET-51851|VSDX إلى PDF - بعض الرموز مفقودة وبعضها لم يتم تقديمه بشكل صحيح|حشرة|
|DIAGRAMNET-51873|VSDX إلى PDF - المحتوى خارج على اليسار في PDF الناتج|حشرة|
|DIAGRAMNET-51874|VSDX إلى PDF - المحتوى والأسطر مفقودة في الإخراج|حشرة|
|DIAGRAMNET-51876|VSDX إلى PNG - بعض الأشكال غير صحيحة في الإخراج|حشرة|
|DIAGRAMNET-51879|Visio إلى PDF - الإخراج غير صحيح|حشرة|
|DIAGRAMNET-51894|System.NullReferenceException أثناء تحميل diagram|حشرة|
|DIAGRAMNET-51895|تعذر استرداد بيانات خاصية المجموعة مثل SelectionModel و DisplayMode|حشرة|

## **عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**  ##
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.

####  تمت إضافة طريقة AddShape في الصفحة ####
```
Diagram diagram = new Diagram();

// Get page object by index
Aspose.Diagram.Page page0 = diagram.Pages[0];
// set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import ole as Visio shape word
page0.AddShape(pinX, pinY, width, hieght, new FileStream( "imageword.emf", FileMode.OpenOrCreate), new FileStream( "wordsource.doc", FileMode.OpenOrCreate));
```
