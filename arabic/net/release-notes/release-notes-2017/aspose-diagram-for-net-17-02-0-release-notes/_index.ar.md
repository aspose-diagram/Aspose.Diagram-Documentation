---
title: Aspose.Diagram for .NET 17.02.0 ملاحظات الإصدار
type: docs
weight: 110
url: /ar/net/aspose-diagram-for-net-17-02-0-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 17.02.0](https://www.nuget.org/packages/Aspose.Diagram/17.2.0).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-50018|تمت إضافة دعم متوافق مع CLS.|ميزة جديدة|
|DIAGRAMNET-51110|متكامل مع متر.|ميزة جديدة|
|DIAGRAMNET-51143|القدرة على الحصول على مجموعة شكل معين.|ميزة جديدة|
|DIAGRAMNET-51144|القدرة على الحصول على والد لشكل معين.|ميزة جديدة|
|DIAGRAMNET-50149|VSD لتحويل PDF ، يتم تغيير ظل لون الخلفية لشكل المجموعة.|حشرة|
|DIAGRAMNET-50579|VSDX لتحويل PDF ، لون خلفية غير صحيح للشكل.|حشرة|
|DIAGRAMNET-50984|خطوط حدود الجدول مفقودة عند تحويل VSDX إلى PNG.|حشرة|
|DIAGRAMNET-50985|لم تتم محاذاة عناصر النص بشكل صحيح عند تحويل VSDX إلى PNG.|حشرة|
|DIAGRAMNET-50999|عرض ألوان غير صحيحة للأشكال عند تحويل VSD إلى PNG.|حشرة|
|DIAGRAMNET-51002|HTMLSaveOptions.DefaultFont الخاصية لا تعمل كما هو متوقع.|حشرة|
|DIAGRAMNET-51049|لا يتم تقديم لون الأشكال بشكل صحيح عند تحويل VSD إلى HTML.|حشرة|
|DIAGRAMNET-51080|محاذاة النص الخاطئة للأشكال عند الحفظ في EMF.|حشرة|
|DIAGRAMNET-51132|يتم تغيير زوايا الشكل المستديرة عند تحويل VSD إلى PDF.|حشرة|
|DIAGRAMNET-51133|يتم تغيير تخطيط موصل السهم الديناميكي عند تحويل VSD إلى PDF.|حشرة|
|DIAGRAMNET-51135|يتم إزاحة الأشكال Visio عند تحويل VSDX إلى PDF.|حشرة|
|DIAGRAMNET-51136|يظهر النص الرأسي كنص أفقي عند تحويل VSDX إلى PDF.|حشرة|
|DIAGRAMNET-51140|مربع النص العمودي يتدلى من حافة العقدة أثناء تحويل VSDX إلى PDF.|حشرة|
|DIAGRAMNET-51138|حدث خطأ أثناء تحميل diagram VSDX.|استثناء|
|DIAGRAMNET-51139|حدث خطأ لا يمكن الوصول إلى الملف عند تحويل VSDX إلى HTML.|استثناء|
|DIAGRAMNET-51148|NullReferenceException في Diagram. احفظ أثناء تحويل VSD إلى HTML.|استثناء|
|DIAGRAMNET-51149|NullReferenceException في Diagram. احفظ عندما لا يتم تعيين خاصية CustomProp.Name|استثناء|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
 فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف خاصية Shape.ParentShape**
تسمح الخاصية Shape.ParentShape بالحصول على الشكل الأصل لشكل حديث.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the VSD diagram

Diagram diagram = new Diagram("Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);

Shape parentShape = shape.ParentShape;

Console.WriteLine("Parent Shape's Properties:");

Console.WriteLine("Shape ID: " + parentShape.ID);

Console.WriteLine("Shape Name: " + parentShape.Name);

Console.WriteLine("Shape Type: " + parentShape.Type);

{{< /highlight >}}
### **يضيف Shape.IsInGroup طريقة**
تسمح طريقة Shape.IsInGroup باكتشاف ما إذا كان الشكل الأخير جزءًا من أي شكل مجموعة.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the VSD diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);

Console.WriteLine("Is it in a Group: " + shape.IsInGroup());

{{< /highlight >}}
### **يضيف فئة المقننة**
تمت إضافة فئة المقننة. يسمح للمطورين بإلغاء تأمين قيود التقييم لـ Aspose.Diagram API بالإضافة إلى تعقب تراخيص API والحفاظ عليها. كما تراقب الاستخدام المنتظم لـ Aspose.Diagram API.

{{< highlight "java" >}}

 // Initialize a Metered license class object

Aspose.Diagram.Metered metered = new Aspose.Diagram.Metered();

// apply public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [قم بتعيين المفاتيح العامة والخاصة لتطبيق الترخيص المقنن](/diagram/ar/net/licensing/#licensing-setpublicandprivatekeystoapplymeteredlicense)
1. [استرجع الشكل الأصلي لشكل فرعي](/diagram/ar/net/add-retrieve-copy-and-read-visio-shape-data/#add-retrieve-copyandreadvisioshapedata-retrievetheparentshapeofasub-shape)
1. [تحقق مما إذا كان الشكل Visio في مجموعة من الأشكال](https://docs.aspose.com/diagram/net/group-convert-and-verify-shapes/)
