---
title: قم بتعيين Visio شكل XForm و Line و Fill Data
type: docs
weight: 20
url: /ar/net/set-visio-shape-s-xform-line-and-fill-data/
description: يشرح هذا القسم كيفية تعيين نمط الشكل بما في ذلك بيانات الخط وملء البيانات بـ Aspose.Diagram.
---
## **ضبط بيانات XForm**
 عنصر XForm هو جزء من Microsoft Visio مخطط XML. يحدد XForm موضع الأشكال ، على سبيل المثال العرض والارتفاع والدوران وما إذا كان الشكل قد انعكس. ال[XForm](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) الممتلكات التي يتعرض لها[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) فئة ، يدعم كائن Aspose.Diagram.XForm. يمكن استخدام الخاصية XForm لاسترداد بيانات XForm للشكل أو تحديثها. تعمل أمثلة التعليمات البرمجية في هذه المقالة على تغيير قيم PinX (إحداثيات س) و PinY (إحداثيات ص) لتحريك الأشكال على الصفحة.

عملية تحديث بيانات XForm هي:

1. قم بتحميل diagram. # ابحث عن شكل معين # قم بتحديث بيانات XForm للشكل.
1. احفظ diagram.
### **عينة البرمجة**
يوضح مقتطف الشفرة أدناه كيفية تحديث بيانات XForm للشكل. يبحث الكود عن عملية أسماء الأشكال ، بمعرف الشكل 1 ، ويضبط إحداثياته X و Y على 5.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetXFormdata-SetXFormdata.cs" >}}
## **قم بتعيين Visio بيانات خط الشكل**
يمكن تنسيق الأشكال بعدة طرق. توضح هذه المقالة كيفية تحديد سمات السطر.

Microsoft Visio يتيح للمستخدمين تنسيق السطور بعدة طرق. Aspose.Diagram for .NET يدعم:

- الوزن: سمك الخط.
- اللون: تعيين لون خط الشكل.
- شفافية لون الخط: اضبط شفافية لون خط الشكل بالنسبة المئوية.
- النمط: يحدد ما إذا كان الخط متصلًا أم متقطعًا أم له نمط آخر.
- التقريب: نصف قطر الزوايا.
- أسهم البداية والنهاية: تحدد ما إذا كان السطر يحتوي على أسهم أم لا.
- أحجام أسهم البداية والنهاية: قم بتعيين أحجام الأسهم.
- الغطاء: تقريب الخط ينتهي.
### **تغيير لون الخط والوزن ونوع الشرطة والشفافية والتقريب ونوع السهم وحجم السهم لحد الشكل**
 ال[خط](http://www.aspose.com/api/net/diagram/aspose.diagram/line) الممتلكات التي يتعرض لها[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)فئة ، تدعم كائن Aspose.Diagram.Line. يمكن استخدام هذه الخاصية لاسترداد بيانات خط الشكل أو تحديثها.
#### **عينة برمجة بيانات الخط**
يقوم الجزء التالي من التعليمات البرمجية بتحديث بيانات خط الشكل.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetLineData-SetLineData.cs" >}}
## **قم بتعيين Visio بيانات تعبئة الشكل**
 يمكن تنسيق الأشكال بعدة طرق. يصف هذا الموضوع كيفية تحديد تعبئة الشكل. Microsoft Office Visio يتيح للمستخدمين تنسيق التعبئة بطرق مختلفة. ال[يملأ](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) فئة Aspose.Diagram for .NET API تدعم الإعداد:

- ألوان الخلفية والمقدمة.
- الشفافية.
- أنماط التعبئة.
- الظلال.
### **ضبط قيم التعبئة**
 خاصية Fill ، المكشوفة بواسطة[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) الطبقة ، يدعم[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) هدف. يمكن استخدام الخاصية Fill لاسترداد بيانات تعبئة الشكل أو تحديثها.
#### **تعبئة نموذج لبرمجة البيانات**
يقوم مقتطف التعليمات البرمجية التالي بتحديث بيانات تعبئة الشكل. تبحث الشفرة عن شكل يسمى مستطيل ، بمعرف الشكل 1 ، وتعيين خلفية التعبئة وألوان المقدمة.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetFillData-SetFillData.cs" >}}
### **استرجع بيانات التعبئة الموروثة لشكل Visio**
 يمكن أن ترث أشكال Visio النمط الأصل والشكل الرئيسي. يمكن للمطورين الحصول على بيانات التعبئة الموروثة لشكل Visio أو تعيينها. الخاصية InheritFill ، المكشوفة بواسطة[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class ، تحتوي على قيم تنسيق التعبئة للشكل الذي يرثه النمط الأصل والشكل الرئيسي.
#### **استرجاع نموذج برمجة بيانات التعبئة الموروثة**
يسترد مقتطف التعليمات البرمجية التالي بيانات التعبئة الموروثة للشكل. يرجى التحقق من نموذج الكود هذا:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveInheritedFillData-RetrieveInheritedFillData.cs" >}}
