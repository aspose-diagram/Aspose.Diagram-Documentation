---
title: قم بتعيين Visio شكل XForm و Line و Fill Data
type: docs
weight: 70
url: /ar/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **ضبط بيانات XForm**
 عنصر XForm هو جزء من Microsoft Visio مخطط XML. يحدد XForm موضع الأشكال ، على سبيل المثال العرض والارتفاع والدوران وما إذا كان الشكل قد انعكس. ال[XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) الممتلكات التي يتعرض لها[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) فئة ، يدعم كائن Aspose.Diagram.XForm. يمكن استخدام الخاصية XForm لاسترداد بيانات XForm للشكل أو تحديثها. تعمل أمثلة التعليمات البرمجية في هذه المقالة على تغيير قيم PinX (إحداثيات س) و PinY (إحداثيات ص) لتحريك الأشكال على الصفحة.

**المدخلات diagram** 

![ما يجب القيام به: image_بديل_نص](set-visio-shape-s-xform-line-and-fill-data_1.png)

**diagram بعد** **PinX** **و** **بيني** **تم تغيير القيم** 

![ما يجب القيام به: image_بديل_نص](set-visio-shape-s-xform-line-and-fill-data_2.png)

عملية تحديث بيانات XForm هي:

1. قم بتحميل diagram. # ابحث عن شكل معين # قم بتحديث بيانات XForm للشكل.
1. احفظ diagram.
### **عينة البرمجة**
يوضح مقتطف الشفرة أدناه كيفية تحديث بيانات XForm للشكل. يبحث الكود عن عملية أسماء الأشكال ، بمعرف الشكل 1 ، ويضبط إحداثياته X و Y على 5.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetXFormdata-SetXFormdata.java" >}}
## **قم بتعيين Visio بيانات خط الشكل**
يمكن تنسيق الأشكال بعدة طرق. توضح هذه المقالة كيفية تحديد سمات السطر.

Microsoft Visio يتيح للمستخدمين تنسيق السطور بعدة طرق. Aspose.Diagram for Java يدعم:

- الوزن: سمك الخط.
- اللون: تعيين لون خط الشكل.
- شفافية لون الخط: اضبط شفافية لون خط الشكل بالنسبة المئوية.
- النمط: يحدد ما إذا كان الخط متصلًا أم متقطعًا أم له نمط آخر.
- التقريب: نصف قطر الزوايا.
- أسهم البداية والنهاية: تحدد ما إذا كان السطر يحتوي على أسهم أم لا.
- أحجام أسهم البداية والنهاية: قم بتعيين أحجام الأسهم.
- الغطاء: تقريب الخط ينتهي.
### **تغيير لون الخط والوزن ونوع الشرطة والشفافية والتقريب ونوع السهم وحجم السهم لحد الشكل**
 ال[خط](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) الممتلكات التي يتعرض لها[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)فئة ، تدعم كائن Aspose.Diagram.Line. يمكن استخدام هذه الخاصية لاسترداد بيانات خط الشكل أو تحديثها.
#### **عينة برمجة بيانات الخط**
يقوم الجزء التالي من التعليمات البرمجية بتحديث بيانات خط الشكل.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetLineData-SetLineData.java" >}}
## **قم بتعيين Visio بيانات تعبئة الشكل**
يمكن تنسيق الأشكال بعدة طرق. يصف هذا الموضوع كيفية تحديد تعبئة الشكل.

 Microsoft Office Visio يتيح للمستخدمين تنسيق التعبئة بطرق مختلفة. ال[يملأ](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) فئة Aspose.Diagram for Java API تدعم الإعداد:

- ألوان الخلفية والمقدمة.
- الشفافية.
- أنماط التعبئة.
- الظلال.
### **ضبط قيم التعبئة**
تدعم خاصية Fill ، المكشوفة بواسطة فئة Shape ، كائن Aspose.Diagram.Fill. يمكن استخدام الخاصية Fill لاسترداد بيانات تعبئة الشكل أو تحديثها.

|<p>**المدخلات diagram** </p><p>![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/OrhEecb.png)</p>|<p>**diagram بعد تغيير لون التعبئة** </p><p>![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **تعبئة نموذج لبرمجة البيانات**
يقوم مقتطف التعليمات البرمجية التالي بتحديث بيانات تعبئة الشكل. تبحث الشفرة عن شكل يسمى مستطيل ، بمعرف الشكل 1 ، وتعيين خلفية التعبئة وألوان المقدمة.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetFillData-SetFillData.java" >}}
### **استرجع بيانات التعبئة الموروثة لشكل Visio**
يمكن أن ترث أشكال Visio النمط الأصل والشكل الرئيسي. يمكن للمطورين الحصول على بيانات التعبئة الموروثة لشكل Visio أو تعيينها. تحتوي الخاصية InheritFill ، المكشوفة بواسطة فئة الشكل ، على قيم تنسيق التعبئة للشكل الذي يرثه النمط الأصل والشكل الرئيسي.
#### **استرجاع نموذج برمجة بيانات التعبئة الموروثة**
يسترد مقتطف التعليمات البرمجية التالي بيانات التعبئة الموروثة للشكل. يرجى التحقق من نموذج الكود هذا:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveInheritedFillData-RetrieveInheritedFillData.java" >}}
