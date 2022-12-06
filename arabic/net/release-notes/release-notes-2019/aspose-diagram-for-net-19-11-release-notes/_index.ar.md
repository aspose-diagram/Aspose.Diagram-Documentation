---
title: Aspose.Diagram for .NET 19.11 ملاحظات الإصدار
type: docs
weight: 20
url: /ar/net/aspose-diagram-for-net-19-11-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for .NET 19.11.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-50004| أضف الدعم إلى[تطبيق ورقة الأنماط](/diagram/ar/net/format-visio-pages/) للصفحة الكاملة|التعزيز|
|DIAGRAMNET-50576|أضف دعمًا للتخلص من كائن فئة Diagram|التعزيز|
|DIAGRAMNET-50098|تعيين لون خلفية الصفحة|حشرة|
|DIAGRAMNET-51722|Diagram إلى SVG - صورة الإخراج بها عيوب|حشرة|
|DIAGRAMNET-51724|أخطاء في وحدة تحكم Chrome عند عرض إخراج SVG|حشرة|
|DIAGRAMNET-51725|استرجع z-index للأشكال في Diagram|حشرة|
|DIAGRAMNET-51726|فقدان صورة الخلفية (تمت إضافة PowerPoint في VISIO) أثناء إزالة الأشكال والأنماط الرئيسية غير المستخدمة|حشرة|
|DIAGRAMNET-51727|CheckBox (CheckBox Control) مفقود أثناء إزالة الأشكال والأنماط الرئيسية غير المستخدمة|حشرة|
|DIAGRAMNET-51728|الخط مفقود أثناء إزالة الأشكال والأنماط الرئيسية غير المستخدمة|حشرة|

## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.
### **تمت إضافة ApplyStyle في الصفحة**
يطبق النمط على الصفحة الكاملة.

{{< highlight "java" >}}

StyleSheet st = new StyleSheet();

st.ID = dia.StyleSheets.Count + 1;

Aspose.Diagram.Char ch = new Aspose.Diagram.Char();

ch.Color.Value = "#00ff00";

ch.IX = 0;

st.Chars.Add(ch);

st.Line.LineColor.Value = "#ff0000";

st.Line.LinePattern.Value = 1;

st.Line.LineWeight.Value = 0.01;

st.Fill.FillForegnd.Value = "#0000ff";

st.Fill.FillPattern.Value = 1;

st.Fill.ShdwPattern.Value = 0;

dia.StyleSheets.Add(st);

foreach (Shape shape in dia.Pages[0].Shapes)

{

     shape.Line.LinePattern.Value = 1;
    
     shape.Fill.FillPattern.Value = 1;

}

dia.Pages[0].ApplyStyle(st.ID, st.ID, st.ID);

{{< /highlight >}}
### **تمت الإضافة في Diagram**
ينفذ المهام المحددة من قبل التطبيق والمرتبطة بتحرير الموارد غير المُدارة أو تحريرها أو إعادة تعيينها.

{{< highlight "java" >}}

 diagram.Dispose();

{{< /highlight >}}
