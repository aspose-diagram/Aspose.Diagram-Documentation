---
title: Aspose.Diagram for Java 19.11 ملاحظات الإصدار
type: docs
weight: 20
url: /ar/java/aspose-diagram-for-java-19-11-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for Java 19.11.

{{% /alert %}} 
## **التحسينات والتغييرات**
إصدار هذا الشهر يسمح بتنسيق صفحات Visio حسب[تطبيق أوراق الأنماط](/diagram/ar/java/format-visio-pages/).

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50671|لم يتم احترام إعداد نافذة جديدة لورقة الشكل عند التحويل إلى SVG|التعزيز|
### **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفين أو المهملين بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram لـ JAVA. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى طرحه على منتدى الدعم Aspose.Diagram.
### **أضيفت تطبيق نمط في الصفحة**
{{< highlight "java" >}}

 StyleSheet st = new StyleSheet();

dia.getPages().get(0).applyStyle(st.ID, st.ID, st.ID);

{{< /highlight >}}
### ` `**تمت إضافة التخلص في فئة Diagram**
ينفذ المهام المحددة من قبل التطبيق والمرتبطة بتحرير الموارد غير المُدارة أو تحريرها أو إعادة تعيينها.

{{< highlight "java" >}}

 diagram.dispose();

{{< /highlight >}}
