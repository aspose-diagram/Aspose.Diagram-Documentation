---
title: استرجع Visio الموصلات ومعلومات الخط
type: docs
weight: 20
url: /ar/java/retrieve-visio-connectors-and-font-information/
---
## **استرداد معلومات الموصل**
 يوفر Aspose.Diagram for Java آليات لاسترجاع المعلومات - المعرف والاسم - حول[الصفحات](/diagram/ar/java/retrieve-get-copy-and-insert-a-page/) و[رئيسي - سيد](). كما يتيح لك الحصول على معلومات حول الموصلات والعناصر التي تربط الأشكال.

 ال[الاتصال](https://reference.aspose.com/diagram/java/com.aspose.diagram/connect) يمثل الكائن الموصل الذي يربط شكلين على Visio صفحة رسم. الخاصية Connects ، المكشوفة بواسطة[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) فئة تدعم مجموعة من Aspose.Diagram.Connect الكائنات. يمكن استخدام هذه الخاصية لاسترداد معلومات المعرف والاسم حول الموصل.

**تظهر نافذة وحدة التحكم الإخراج من الكود أدناه.** 

![ما يجب القيام به: image_بديل_نص](retrieve-visio-connectors-and-font-information_1.png)
### **عينة البرمجة**
يسترد جزء الكود التالي المعلومات الخاصة بالموصلات في diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RetrieveConnectorInfo-RetrieveConnectorInfo.java" >}}
## **استرداد معلومات الخط**
 Aspose.Diagram لديه آليات لاسترجاع المعلومات حول العناصر التي تشكل diagram ، من[الصفحات](/diagram/ar/java/retrieve-get-copy-and-insert-a-page/), [الإستنسل](), [موصلات](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection)وكذلك الخطوط. يوضح هذا المقال كيفية معرفة الخطوط المستخدمة في diagram.

 ال[الخط](https://reference.aspose.com/diagram/java/com.aspose.diagram/font) يمثل الكائن محرفًا يتم تطبيقه على نص في مستند أو متاح للاستخدام على النظام.

يقوم كائن الخط بتعيين اسم (على سبيل المثال ، "Arial") لمعرف الخط (على سبيل المثال ، 3) الذي يخزنه Microsoft Visio في خلية خط في قسم حرف لشكل يحتوي على نص منسق باستخدام هذا الخط. يمكن أن تتغير معرفات الخطوط عند فتح مستند على أنظمة مختلفة أو عند تثبيت الخطوط أو إزالتها.
### **استرجاع نموذج برمجة الخط**
يسترد جزء الكود التالي معلومات الخط من Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RetrieveFontInfo-RetrieveFontInfo.java" >}}

![ما يجب القيام به: image_بديل_نص](retrieve-visio-connectors-and-font-information_2.png)
### **الحصول على دليل الخطوط الافتراضي**
Aspose.Diagram for Java API يسمح أيضًا بالحصول على مسار دليل الخط الافتراضي باستخدام طريقة getDefaultFontDir () من Diagram Class. يسترد جزء الكود التالي دليل الخط الافتراضي من Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-GetDefaultFontDirectory-GetDefaultFontDirectory.java" >}}
