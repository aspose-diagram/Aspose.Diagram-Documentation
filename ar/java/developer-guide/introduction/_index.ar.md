---
title: مقدمة
type: docs
weight: 10
url: /ar/java/introduction/
---
{{% alert color="primary" %}} 

Microsoft Visio يحفظ معلومات حول الإجراءات التي تم اتخاذها على diagram داخل الملف. على سبيل المثال ، يتم حفظ وقت وتاريخ إنشاء المستند ، وآخر مرة تم فيها تحريره أو طباعته أو حفظه ، مع الملف. يتم أيضًا حفظ المعلومات الخاصة بإصدار Microsoft Visio الذي تم إنشاؤه وإجراء آخر تحرير للملف.

تشرح هذه المقالة كيفية استرداد تلك المعلومات.

{{% /alert %}} 
## **احصل على نسخة مكتبة Aspose.Diagram for Java**
 يتم عرض memthod getVersion () بواسطة ملف[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class وطريقة getBuildNumberCreated () المكشوفة بواسطة[خصائص المستند](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) يتم استخدام الفئة لتحديد الإصدار ورقم البنية الكامل لمثيل Microsoft Visio المستخدم في تكوين الوثيقة.
### **تحديد إصدار Microsoft Visio الذي تم إنشاؤه وتحريره وحفظه في مستند**
 تم الكشف عن طريقة getBuildNumberEdited () بواسطة ملف[خصائص المستند](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) يتم استخدام الفئة لتحديد رقم البنية الكامل لمثيل Microsoft Visio المستخدم لتحرير الوثيقة.

طرق getTimeCreated () و getTimeEdited () و getTimePrinted () و getTimeSaved () المكشوفة بواسطة[خصائص المستند](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) يتم استخدام الفئة لتحديد الوقت الذي تم فيه إنشاء المستند Microsoft Visio ، وآخر تحرير ، وطباعة آخر مرة وحفظها مؤخرًا.

يمكنك أيضًا تعيين هذه الخصائص لتغيير المعلومات الموجودة في الملف.

توضح نماذج التعليمات البرمجية أدناه كيفية استرداد المعلومات حول ما تم إنشاء الملف وكذلك وقت إنشائه وتحريره وطباعته وحفظه.

**إخراج الكود في نافذة وحدة التحكم** 

![ما يجب القيام به: image_بديل_نص](introduction_1.png)
#### **عينة البرمجة**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetLibraryVersion.class);
// build path of an existing diagram
String path = dataDir + "Drawing1.vsdx";

//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(path);

//Display Visio version and document modification time at different stages
System.out.println("Visio Instance Version : " + diagram.getVersion());
System.out.println("Full Build Number Created : " + diagram.getDocumentProps().getBuildNumberCreated());
System.out.println("Full Build Number Edited : " + diagram.getDocumentProps().getBuildNumberEdited());
System.out.println("Date Created : " + diagram.getDocumentProps().getTimeCreated());
System.out.println("Date Last Edited : " + diagram.getDocumentProps().getTimeEdited());
System.out.println("Date Last Printed : " + diagram.getDocumentProps().getTimePrinted());
System.out.println("Date Last Saved : " + diagram.getDocumentProps().getTimeSaved());

{{< /highlight >}}
```
## **كتابة Microsoft Visio معلومات ملخص المستند**
يتيح لك Microsoft Visio تحديد عدد من خصائص معلومات ملخص المستند لمساعدتك وزملاؤك في تحديد diagram. خصائص الملخص ، على سبيل المثال العنوان والموضوع والمؤلف والوصف ، تجعل العثور على الملف أسهل عند البحث ، ويسهل التعرف عليه عند التصفح الملفات.

 ال[خصائص المستند](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties)تعرض فئة عددًا من الخصائص لتعيين معلومات تلخيصية Microsoft Visio diagram أو الحصول عليها. يمكن لـ Aspose.Diagram for Java تحديث معلومات ملخص الرسم ثم إعادة كتابة ملف الرسم إلى VDX.

{{% alert color="primary" %}} 

يرجى ملاحظة أنه لا يمكنك تعيين القيم مقابل**طلب**و**منتج**الحقول ، لأنه سيتم عرض Aspose Ltd. و Aspose.Diagram for Java xxx مقابل هذه الحقول.

{{% /alert %}} 
### **كتابة Microsoft Visio معلومات ملخص المستند**
لتحديث معلومات ملخص الرسم لملف VDX أو VSD موجود:

1.  قم بإنشاء مثيل لـ[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) صف دراسي.
1. قم بتعيين الخصائص المعروضة بواسطة أسلوب Diagram.getDocumentProps () لتعريف معلومات التلخيص لملف الرسم Visio.
1. اتصل بالطريقة Diagram class 'save () لكتابة ملف الرسم Visio إلى VDX.

تحقق من المعلومات الموجزة:

1. افتح ملف الإخراج VDX في Microsoft Visio.
1.  التحديد**معلومات** من**ملف** قائمة.

**يعرض مربع حوار المعلومات معلومات الملخص المحدثة** 

![ما يجب القيام به: image_بديل_نص](introduction_2.png)
#### **عينة البرمجة**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetVisioProperties.class);
// build path of an existing diagram
String path = dataDir + "Drawing1.vsdx";

//Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(path);

//Set some summary information about the diagram
diagram.getDocumentProps().setCreator("Ijaz");
diagram.getDocumentProps().setCompany("Aspose");
diagram.getDocumentProps().setCategory("Drawing 2D");
diagram.getDocumentProps().setManager("Sergey Polshkov");
diagram.getDocumentProps().setTitle("Aspose Title");
diagram.getDocumentProps().setTimeCreated(DateTime.getNow());
diagram.getDocumentProps().setSubject("Visio Diagram");
diagram.getDocumentProps().setTemplate("Aspose Template");

//Write the updated file to the disk in VSDX file format
diagram.save(dataDir + "SetVisioProperties_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **كشف تنسيق ملف Visio**
 استخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API ، يمكن للمطورين اكتشاف تنسيق الملف Visio قبل فتحه لأن امتداد الملف لا يضمن أن محتوى الملف مناسب.
### **كشف نموذج برمجة التنسيق**
يوضح نموذج التعليمات البرمجية التالي كيفية اكتشاف تنسيق ملف (باستخدام مسار الملف أو دفقه) والتحقق من امتداده.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectVisioFileFormat.class);

		// detect file format using the direct file path
		FileFormatInfo info = FileFormatUtil.detectFileFormat(dataDir + "Drawing1.vsdx");

		// get the detected file format
		System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}
```
## **كشف تنسيق ملف Visio من InputStream**
باستخدام Aspose.Diagram for Java API ، يمكن للمطورين اكتشاف تنسيق ملف Visio عن طريق تمرير تدفق الإدخال. يمكن استخدام طريقة DiscoverFileFormat لفئة FileFormatUtil لتحقيق ذلك.
### **كشف التنسيق من نموذج برمجة InputStream**
يوضح نموذج التعليمات البرمجية التالي كيفية اكتشاف تنسيق ملف باستخدام دفق الإدخال.

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
