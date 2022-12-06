---
title: Aspose.Diagram for Java 17.6 ملاحظات الإصدار
type: docs
weight: 70
url: /ar/java/aspose-diagram-for-java-17-6-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for Java 17.6](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-6-release-notes/).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50500|الناتج VSDX - لم يتم تغيير حجم الشكل المضاف يدويًا|التعزيز|
|DIAGRAMJAVA-50503|المخرج VSDX - تجاوز النص عند إضافة نص متعدد الأسطر|التعزيز|
|DIAGRAMJAVA-50505|حدث خطأ مؤشر فارغ عند تحويل صفحة الرسم إلى صورة|حشرة|
|DIAGRAMJAVA-50484|عرض نص عمودي لشكل مربع القرار عند حفظ رسم بتنسيق VSDX|حشرة|
|DIAGRAMJAVA-50486|عرض نص عمودي لشكل العملية المعرفة مسبقًا عند حفظ رسم بتنسيق VSDX|حشرة|
|DIAGRAMJAVA-50492|لا يتم الاحتفاظ بالصيغ الموجودة في خلايا العرض والارتفاع|حشرة|
|DIAGRAMJAVA-50493|الأحرف المفقودة عند تحويل VSD إلى SVG|حشرة|
|DIAGRAMJAVA-50494|الناتج VSDX - خطوط التوصيل غير متصلة في منتصف أشكال العملية|حشرة|
|DIAGRAMJAVA-50499|VSDX إلى PNG - يظهر خط أفقي أبيض أسفل الشكل|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
راجع قائمة أي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفين أو المهملين بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه على[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف طريقة RefreshData في فئة Shape**
تسمح طريقة Shape.refreshData للمطورين بتحديث البيانات بعد تغيير موضع الشكل ونص الشكل و Geoms والوصلات.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

//Find a particular shape and update its XForm

for(Shape shape :(Iterable<Shape>) diagram.getPages().get(0).getShapes())

{

    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)

    {

        shape.getXForm().getPinX().setValue(5);

        shape.getXForm().getPinY().setValue(5);

        shape.refreshData();

    }

}

{{< /highlight >}}
