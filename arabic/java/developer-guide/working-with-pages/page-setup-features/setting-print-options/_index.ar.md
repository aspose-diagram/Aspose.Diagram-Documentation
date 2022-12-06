---
title: ضبط خيارات الطباعة
type: docs
weight: 10
url: /ar/java/setting-print-options/
description: يوضح هذا القسم كيفية تعيين خيارات الطباعة باستخدام Aspose.Diagram.
---
{{% alert color="primary" %}}

في بعض الأحيان ، من الضروري تكوين إعدادات إعداد الصفحة للصفحات للتحكم في الطباعة. توفر إعدادات إعداد الصفحة هذه خيارات متنوعة.

{{% /alert %}}

## **ضبط خيارات الطباعة**

خيارات إعداد الصفحة مدعومة بالكامل في Aspose.Diagram. تشرح هذه المقالة كيفية تعيين خيارات الصفحة مع Aspose.Diagram وتعرض نماذج التعليمات البرمجية للإعداد:

 Aspose.Diagram يوفر فصل دراسي ،[**صفحة**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) ، هذا يمثل ملف Microsoft Visio. ال[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) فئة تحتوي على[**الصفحات**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection) مجموعة تتيح الوصول إلى كل صفحة في ملف Visio. يتم تمثيل الصفحة بواسطة[**صفحة**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)صف دراسي.

 ال[**ورقة الصفحة**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) فئة توفر[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) الخاصية المستخدمة لتعيين خيارات إعداد الصفحة للصفحة. في الواقع ، هذا[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) الخاصية هي كائن من[**ورقة الصفحة**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) فئة تستخدم لتعيين خيارات تخطيط صفحة مختلفة لصفحة مطبوعة. ال[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)توفر فئة الخصائص المختلفة المستخدمة لتعيين خيارات إعداد الصفحة. تمت مناقشة بعض هذه الخصائص أدناه.

### **اتجاه طباعة الصفحة**

 يمكن ضبط اتجاه طباعة الصفحة على الوضع الرأسي أو الأفقي باستخدام ملف[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) صف دراسي'[**PrintPageOrientation**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) منشأه. ال[**PrintPageOrientation**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) تقبل الخاصية إحدى القيم المحددة مسبقًا في ملف[**PrintPageOrientationValue**](https://reference.aspose.com/diagram/java/com.aspose.diagram/PrintPageOrientationValue)التعداد ، المدرجة أدناه.

|**طباعة أنواع اتجاه الصفحة**|**وصف**|
|:- |:- |
|SameAsPrinter|نفس اتجاه الطابعة|
|المناظر الطبيعيه|اتجاه أفقي|
|لَوحَة|اتجاه عمودي|

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-SetPageOrientation-SetPageOrientation.java" >}}

### **عامل التحجيم**

 من الممكن تصغير حجم الصفحة أو تكبيره عن طريق ضبط عامل التحجيم بامتداد[**سكيل إكس**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#ScaleX)منشأه.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-SetPageOrientation-SetPageScale.java" >}}
