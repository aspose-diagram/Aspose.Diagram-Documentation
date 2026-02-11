---
title: إدارة خصائص الوثيقة
linktitle: خصائص المستند
type: docs
weight: 80
url: /ar/java/document-properties/
aliases: [/java/document-properties/]
description: إدارة خصائص الوثيقة لملفات visio.
---
## **مقدمة**

يوفر Microsoft Visio إمكانية إضافة خصائص إلى ملفات visio. توفر خصائص المستند هذه معلومات مفيدة وهي مقسمة إلى فئتين كما هو مفصل أدناه.

- الخصائص المحددة من قبل النظام (المضمنة): تحتوي الخصائص المضمنة على معلومات عامة حول المستند مثل عنوان المستند واسم المؤلف وإحصائيات المستند وما إلى ذلك.
- الخصائص المعرفة من قبل المستخدم (المخصصة): الخصائص المخصصة التي يحددها المستخدم النهائي في شكل زوج الاسم والقيمة.

{{% alert color="primary" %}}

أهم نقطة يجب معرفتها حول الخصائص المضمنة والمخصصة هي أنه يمكن الوصول إلى الخصائص المضمنة وتعديلها ، ولكن لا يتم إنشاؤها أو إزالتها. ومع ذلك ، يمكن إنشاء الخصائص المخصصة وإدارتها.

{{% /alert %}}

## **إدارة خصائص الوثيقة باستخدام Microsoft Visio**

 Microsoft Visio يسمح لك بإدارة خصائص الوثيقة لملفات Visio بطريقة WYSIWYG. يرجى اتباع الخطوات التالية لفتح ملف**الخصائص** الحوار Visio 2016.

1.  من**ملف** القائمة ، حدد**معلومات**.

|**اختيار قائمة المعلومات**|
|:- |
|![ما يجب القيام به: image_بديل_نص](managing-document-properties_1.png)|
1.  انقر فوق**الخصائص** العنوان وحدد "خصائص متقدمة".

|**النقر فوق تحديد الخصائص المتقدمة**|
|:- |
|![ما يجب القيام به: image_بديل_نص](managing-document-properties_2.png)|
1. إدارة خصائص وثيقة الملف.

|**حوار الخصائص**|
|:- |
|![ما يجب القيام به: image_بديل_نص](managing-document-properties_3.png)|
في مربع حوار الخصائص ، توجد علامات تبويب مختلفة ، مثل عام ، وملخص ، وإحصاءات ، ومحتويات ، وعادات. تساعد كل علامة تبويب في تكوين أنواع مختلفة من المعلومات المتعلقة بالملف. يتم استخدام علامة التبويب "مخصص" لإدارة الخصائص المخصصة.

## **التعامل مع خصائص الوثيقة باستخدام Aspose.Diagram**

يمكن للمطورين إدارة خصائص الوثيقة ديناميكيًا باستخدام Aspose.Diagram APIs. تساعد هذه الميزة المطورين على تخزين المعلومات المفيدة مع الملف ، مثل وقت استلام الملف ومعالجته وختمه بالوقت وما إلى ذلك.

{{% alert color="primary" %}}

Aspose.Diagram for Java يكتب مباشرة المعلومات حول API ورقم الإصدار في وثائق المخرجات.

يرجى ملاحظة أنه لا يمكنك توجيه Aspose.Diagram for Java لتغيير أو إزالة هذه المعلومات من مستندات الإخراج.

{{% /alert %}}

### **الوصول إلى خصائص المستند**

 تدعم واجهات برمجة التطبيقات Aspose.Diagram كلا نوعي خصائص المستند المضمنة والمخصصة. Aspose.Diagram '[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class يمثل ملف Visio ومثل ملف visio ، فإن ملف[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) يمكن أن تحتوي الفئة على صفحات متعددة ، يمثل كل منها[**صفحة**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class بينما يتم تمثيل مجموعة الصفحات بواسطة[**PageCollection**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection)صف دراسي.

 استخدم ال[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram)للوصول إلى خصائص مستند الملف كما هو موضح أدناه.

- للوصول إلى خصائص المستند المضمنة ، استخدم[**diagram.DocumentProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/documentproperties).
-  للوصول إلى خصائص المستند المخصصة ، استخدم[**diagram.DocumentProps.CustomProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/CustomPropCollection).

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}
```

### **إضافة أو إزالة خصائص المستند المخصصة**

كما أوضحنا سابقًا في بداية هذا الموضوع ، لا يمكن للمطورين إضافة أو إزالة الخصائص المضمنة لأن هذه الخصائص محددة من قبل النظام ولكن من الممكن إضافة أو إزالة الخصائص المخصصة لأنها محددة من قبل المستخدم.

### **إضافة خصائص مخصصة**

 كشفت واجهات برمجة التطبيقات Aspose.Diagram ملف[**يضيف**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection#add(com.aspose.diagram.CustomProp) ) طريقة لـ[**CustomPropCollection**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection)class لإضافة خصائص مخصصة إلى المجموعة.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}
```

### **إزالة الخصائص المخصصة**

 لإزالة الخصائص المهيأة باستخدام Aspose.Diagram ، قم باستدعاء[**CustomPropCollection.Remove**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection#remove(com.aspose.diagram.CustomProp)) وتمرير اسم خاصية المستند المراد إزالتها.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}
```
