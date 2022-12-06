﻿---
title: استرجع Visio الموصلات ومعلومات الخط
type: docs
weight: 20
url: /ar/net/retrieve-visio-connectors-and-font-information/
description: يشرح هذا القسم كيفية الحصول على visio موصلات ومعلومات الخط.
---
## **استرداد معلومات الموصل**
 يوفر Aspose.Diagram for .NET آليات لاسترجاع المعلومات - المعرف والاسم - حول[الصفحات](/diagram/ar/net/retrieve-2c-get-2c-copy-and-insert-a-page/) و[رئيسي - سيد](https://docs.aspose.com/diagram/net/working-with-masters/). كما يتيح لك الحصول على معلومات حول الموصلات والعناصر التي تربط الأشكال.

 ال[الاتصال](http://www.aspose.com/api/net/diagram/aspose.diagram/connect) يمثل الكائن الموصل الذي يربط شكلين على Visio صفحة رسم. الخاصية Connects ، المكشوفة بواسطة[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) فئة تدعم مجموعة من Aspose.Diagram.Connect الكائنات. يمكن استخدام هذه الخاصية لاسترداد معلومات المعرف والاسم حول الموصل.
### **عينة البرمجة**
يسترد جزء الكود التالي المعلومات الخاصة بالموصلات في diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveConnectorInfo-RetrieveConnectorInfo.cs" >}}
## **استرداد معلومات الخط**
 Aspose.Diagram لديه آليات لاسترجاع المعلومات حول العناصر التي تشكل diagram ، من[الصفحات](/diagram/ar/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [الإستنسل](https://docs.aspose.com/diagram/net/working-with-masters/), [موصلات](/diagram/ar/net/retrieving-connector-information/)وكذلك الخطوط. يوضح هذا المقال كيفية معرفة الخطوط المستخدمة في diagram.

 ال[الخط](http://www.aspose.com/api/net/diagram/aspose.diagram/font) يمثل الكائن محرفًا يتم تطبيقه على نص في مستند أو متاح للاستخدام على النظام. يقوم كائن الخط بتعيين اسم (على سبيل المثال ، "Arial") لمعرف الخط (على سبيل المثال ، 3) الذي يخزنه Microsoft Visio في خلية خط في قسم حرف لشكل يحتوي على نص منسق باستخدام هذا الخط. يمكن أن تتغير معرفات الخطوط عند فتح مستند على أنظمة مختلفة أو عند تثبيت الخطوط أو إزالتها.
### **استرجاع نموذج برمجة الخط**
يسترد جزء الكود التالي معلومات الخط من Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveFontInfo-RetrieveFontInfo.cs" >}}
### **الحصول على دليل الخطوط الافتراضي**
Aspose.Diagram for .NET API يسمح أيضًا بالحصول على مسار دليل الخط الافتراضي باستخدام طريقة GetDefaultFontDir () من Diagram Class. يسترد جزء الكود التالي دليل الخط الافتراضي من Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-GetDefaultFontDirectory-GetDefaultFontDirectory.cs" >}}
### **الحصول على خطوط غير مستخدمة**
{{% alert color="primary" %}}

هذه الطريقة مدعومة في الإصدار 19.6 أو أحدث.

{{% /alert %}}

Aspose.Diagram for .NET API يسمح أيضًا بالحصول على الخطوط غير المستخدمة باستخدام طريقة GetUnusedStyles () من Diagram Class. يسترد جزء الكود التالي الخطوط غير المستخدمة من Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-GetUnusedFonts-1.cs" >}}
