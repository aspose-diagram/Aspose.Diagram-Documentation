---
title: إدارة خصائص الوثيقة
linktitle: خصائص المستند
type: docs
weight: 80
url: /ar/net/document-properties/
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

Aspose.Diagram for .NET يكتب مباشرة المعلومات حول API ورقم الإصدار في وثائق المخرجات.

يرجى ملاحظة أنه لا يمكنك توجيه Aspose.Diagram for .NET لتغيير أو إزالة هذه المعلومات من مستندات الإخراج.

{{% /alert %}}

### **الوصول إلى خصائص المستند**

 تدعم واجهات برمجة التطبيقات Aspose.Diagram كلا نوعي خصائص المستند المضمنة والمخصصة. Aspose.Diagram '[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram) class يمثل ملف Visio ومثل ملف visio ، فإن ملف[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram) يمكن أن تحتوي الفئة على صفحات متعددة ، يمثل كل منها[**صفحة**](https://reference.aspose.com/diagram/net/aspose.diagram/page) class بينما يتم تمثيل مجموعة الصفحات بواسطة[**PageCollection**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection)صف دراسي.

 استخدم ال[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram)للوصول إلى خصائص مستند الملف كما هو موضح أدناه.

- للوصول إلى خصائص المستند المضمنة ، استخدم[**diagram.DocumentProps**](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties).
-  للوصول إلى خصائص المستند المخصصة ، استخدم[**diagram.DocumentProps.CustomProps**](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties/properties/customprops).


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//// Display Visio version and document modification time at different stages 
Console.WriteLine("Visio Instance Version : " + diagram.Version);
Console.WriteLine("Full Build Number Created : " + diagram.DocumentProps.BuildNumberCreated);
Console.WriteLine("Full Build Number Edited : " + diagram.DocumentProps.BuildNumberEdited);
Console.WriteLine("Date Created : " + diagram.DocumentProps.TimeCreated);
Console.WriteLine("Date Last Edited : " + diagram.DocumentProps.TimeEdited);
Console.WriteLine("Date Last Printed : " + diagram.DocumentProps.TimePrinted);
Console.WriteLine("Date Last Saved : " + diagram.DocumentProps.TimeSaved);
Console.WriteLine("CustomProps Length " + diagram.DocumentProps.CustomProps.Count);

{{< /highlight >}}


### **إضافة أو إزالة خصائص المستند المخصصة**

كما أوضحنا سابقًا في بداية هذا الموضوع ، لا يمكن للمطورين إضافة أو إزالة الخصائص المضمنة لأن هذه الخصائص محددة من قبل النظام ولكن من الممكن إضافة أو إزالة الخصائص المخصصة لأنها محددة من قبل المستخدم.

### **إضافة خصائص مخصصة**

 كشفت واجهات برمجة التطبيقات Aspose.Diagram ملف[**يضيف**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection/methods/add) طريقة ل[**CustomPropCollection**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection)class لإضافة خصائص مخصصة إلى المجموعة.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//// Get CustomProperties of diagram
Aspose.Diagram.CustomPropCollection customProperties = diagram.DocumentProps.CustomProps;
//Set property of CustomProp
Aspose.Diagram.CustomProp customProp = new Aspose.Diagram.CustomProp();
customProp.PropType = Aspose.Diagram.PropType.String;
customProp.CustomValue.ValueString = "Test";
//Add CustomProp to Collection
customProperties.Add(customProp);

{{< /highlight >}}


### **إزالة الخصائص المخصصة**

 لإزالة الخصائص المهيأة باستخدام Aspose.Diagram ، قم باستدعاء[**CustomPropCollection.Remove**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection/methods/remove)الطريقة وتمرير اسم خاصية المستند المراد إزالتها.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RemovingCustomProperties.cs" >}}
