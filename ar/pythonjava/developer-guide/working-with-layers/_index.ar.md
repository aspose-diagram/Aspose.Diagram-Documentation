---
title: العمل مع الطبقات
type: docs
weight: 160
url: /ar/python-java/working-with-layers/
---
### **تكوين كائنات الشكل مع الطبقات**
يسمح Aspose.Diagram لـ Python via Java بتكوين كائنات الشكل بطبقات في Microsoft Office Visio diagram يمكن أن ينتمي كل شكل إلى طبقات متعددة حتى يتمكن المطورون من إدارة الأشكال لتناسب احتياجات المستخدم النهائي.

 ال[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) يقدم كائن الفئة خاصية LayerMember التي تسمح بإضافة / إزالة كائنات الشكل من / إلى الطبقات في رسم Visio. يمكن للمستخدمين إدارة هذه الخصائص برمجيًا باستخدام Aspose.Diagram API على النحو التالي:

**قم بإضافة وإزالة وتحريك كائنات الشكل من / إلى طبقات diagram.** 

يساعد الجزء التالي من التعليمات البرمجية على إضافة خصائص كائنات الشكل وإزالتها ونقلها.
#### **عينات البرمجة**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-ConfigureShapeLayers.py" >}}
### **أضف طبقة في Visio PageSheet**
Aspose.Diagram لـ Python via Java يسمح للمطورين بإضافة طبقات جديدة لتنظيم فئات مخصصة من الأشكال ، ثم تخصيص أشكال لتلك الطبقات برمجيًا.

 ال[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) يقدم class طريقة إضافة تسمح بإضافة ملف[طبقة](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) كائن فئة في[الرسم Visio](DrawingFlowChart.vsdx). يمكن للمطورين تعيين خصائص الطبقة عن طريق تهيئة كائن الفئة الخاص بها.

يساعد الجزء التالي من التعليمات البرمجية على إضافة كائنات الطبقة.
#### **عينات البرمجة**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-AddLayer.py" >}}

{{% alert color="primary" %}} 

Aspose.Diagram لـ Python via Java يمنح المطورين الوصول إلى الطبقات الموجودة Visio diagram.

{{% /alert %}} 
### **احصل على جميع الطبقات المتاحة**
 ال[ورقة الصفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) ممتلكات[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) تسمح class باسترداد قائمة الطبقات المتاحة من[الرسم Visio](DrawingFlowChart.vsdx) استخدام[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) صف دراسي.

يساعد الجزء التالي من التعليمات البرمجية في الحصول على قائمة الطبقات.
#### **عينات البرمجة**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-RetrieveAllLayers.py" >}}
