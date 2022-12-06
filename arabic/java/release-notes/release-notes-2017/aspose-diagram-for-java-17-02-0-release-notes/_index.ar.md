---
title: Aspose.Diagram for Java 17.02.0 ملاحظات الإصدار
type: docs
weight: 110
url: /ar/java/aspose-diagram-for-java-17-02-0-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for Java 17.02.0](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-02-release-notes/).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50037|VSD لتحويل PDF ، يتم تغيير ظل لون الخلفية لشكل المجموعة.|حشرة|
|DIAGRAMJAVA-50365|يتم إنشاء صفحة فارغة أثناء تحويل صفحة Visio مع المعادلات إلى PNG.|حشرة|
|DIAGRAMJAVA-50461|الحدود مفقودة أثناء تحويل VSDX إلى PNG.|حشرة|
|DIAGRAMJAVA-50462|يختفي الرمز أثناء تحويل VSDX إلى PNG.|حشرة|
|DIAGRAMJAVA-50463|يختفي الرمز أثناء تحويل VSDX إلى SVG.|حشرة|
|DIAGRAMJAVA-50465|يختلف لون النص أثناء تحويل VSDX إلى PNG.|حشرة|
|DIAGRAMJAVA-50466|يكون موضع النص غير صحيح عند تحويل VSD إلى تنسيق SVG.|حشرة|
|DIAGRAMJAVA-50237|` ` [VSDX to PDF] - ظهرت رسالة خطأ عند استخدام الخط العادي LeagueGothic.|استثناء|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
راجع قائمة أي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفين أو المهملين بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه على[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف طريقة Shape.getParentShape**
تسمح طريقة Shape.getParentShape بالحصول على الشكل الأصل لشكل حديث.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the Visio drawing

Diagram diagram = new Diagram("Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);

Shape parentShape = shape.getParentShape();

System.out.println("Parent Shape's Properties:");

System.out.println("Shape ID: " + parentShape.getID());

System.out.println("Shape Name: " + parentShape.getName());

System.out.println("Shape Type: " + parentShape.getType());

{{< /highlight >}}
### **يضيف طريقة Shape.isInGroup**
تسمح طريقة Shape.isInGroup باكتشاف ما إذا كان الشكل الأخير جزءًا من أي شكل مجموعة.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the Visio drawing

Diagram diagram = new Diagram("Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);

System.out.println("Is it in a Group: " + shape.isInGroup());

{{< /highlight >}}
### **يضيف فئة المقننة**
تمت إضافة فئة المقننة. يسمح للمطورين بإلغاء تأمين قيود التقييم لـ Aspose.Diagram API بالإضافة إلى تعقب تراخيص API والحفاظ عليها. كما تراقب الاستخدام المنتظم لـ Aspose.Diagram API.

{{< highlight "java" >}}

 // Initialize a Metered license class object

Metered metered = new Metered();

// apply public and private keys

metered.setMeteredKey("your-public-key", "your-private-key");

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [قم بتعيين المفاتيح العامة والخاصة لتطبيق الترخيص المقنن](/diagram/ar/java/licensing/#licensing-setpublicandprivatekeystoapplymeteredlicense)
1. [استرجع الشكل الأصلي لشكل فرعي](/diagram/ar/java/add-retrieve-copy-and-read-visio-shape-data/#add-retrieve-copyandreadvisioshapedata-retrievetheparentshapeofasub-shape)
1. [تحقق مما إذا كان الشكل Visio في مجموعة من الأشكال](https://docs.aspose.com/diagram/java/group-convert-and-verify-shapes/)


