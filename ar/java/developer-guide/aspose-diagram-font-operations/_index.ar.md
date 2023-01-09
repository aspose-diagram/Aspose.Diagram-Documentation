---
title: Aspose.Diagram عمليات الخط
type: docs
weight: 170
url: /ar/java/aspose-diagram-font-operations/
---
{{% alert color="primary" %}} 

يسمح Aspose.Diagram للمطورين بتعيين أدلة الخط للتصيير في الرسوم التخطيطية Visio. يوضح هذا المقال كيفية استخدام الخطوط من الدلائل المخصصة.

{{% /alert %}} 
### **العمل مع الخطوط**
#### **حيث يبحث Aspose.Diagram عن خطوط TrueType على Windows**
 Aspose.Diagram يبحث عن الخطوط في**Windows \ الخطوط** مجلد. يعمل هذا الإعداد الافتراضي في معظم الأوقات ، لذا حدد مجلدات الخطوط الخاصة بك فقط إذا كنت تريد ذلك حقًا.
#### **كيفية تحديد مجلد الخطوط بشكل صريح**
 كشفت واجهات برمجة التطبيقات Aspose.Diagram طريقة setFontDirs لـ[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) فئة لتحديد مجلدات الخطوط كما هو موضح أدناه.

1. تأخذ طريقة Diagram.setFontDirs مصفوفة سلسلة كمعامل ، لذلك قد يحدد المطور العديد من دلائل الخطوط باستخدام هذا الأسلوب.

{{% alert color="primary" %}} 

عند تحديد مجلد الخطوط باستخدام الطريقة المذكورة أعلاه ، نوصي بتعيين موقع الخط في بداية التطبيق وإلا فقد تتلقى نتائج سيئة التنسيق.

{{% /alert %}} {{% alert color="primary" %}} 

لا يضمن ضبط مجلد الخطوط باستخدام أي من الطرق المذكورة أعلاه أن Aspose.Diagram API لن يبحث عن الخطوط في المواقع الافتراضية مثل مجلد خطوط النظام.

{{% /alert %}} 

يوضح كيفية تعيين Aspose.Diagram للبحث في مجلدات متعددة عن خطوط TrueType عند عرض الخطوط أو دمجها.
#### **عينة البرمجة**
يوضح مثال الكود أدناه كيفية تعيين Aspose.Diagram للبحث في مجلدات متعددة عن خطوط TrueType عند عرض الخطوط أو دمجها.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Fonts-SpecifyFontLocation-SpecifyFontLocation.java" >}}
### **تلقي إعلام بالخطوط المفقودة واستبدال الخط أثناء التقديم**
يتطلب Aspose.Diagram API الوصول إلى الخط الدقيق من أجل تقديم الرسم بشكل صحيح إلى تنسيق PDF. إذا لم يكن الخط المطلوب متاحًا على الجهاز ، فإن Aspose.Diagram API يعرض أي مثيل لهذا الخط باستخدام الخط الافتراضي أو أقرب خط متاح على الجهاز ، نظرًا لأن هذا الاستبدال يمكن أن يغير مظهر الرسم المعروض ، فقد يحتاج المطورون إلى ذلك يتم إعلامك عند فقد الخط وبأي خط سيتم استبداله.
#### **إعلام بالخطوط المفقودة وعينة برمجة استبدال الخطوط**
ليتم إعلامك باستبدال الخط أثناء العرض:

1. قم بإنشاء فصل دراسي يقوم بتنفيذ[IWarning استدعاء](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)
1. قم بتمريره إلى خاصية PdfSaveOptions.setWarningCallback (com.aspose.diagram.IWarningCallback).

أثناء حفظ مثيل الرسم[IWarning استدعاء](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)يتم استدعاؤه في حالة وجود أي مشكلات محتملة تتعلق بالإخلاص في الرسم. في هذه الحالة ، نختار فقط معالجة التحذيرات الخاصة باستبدال الخط وطباعة التحذير على الشاشة. يوضح المثال أدناه كيفية تلقي إعلامات باستبدال الخطوط باستخدام[IWarning استدعاء](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback).

**Java**

{{< highlight "java" >}}

 // load the document to render.

Diagram diagram = new Diagram("C:\\temp\\Output.vsdx");


// initialize PdfSaveOptions object

com.aspose.diagram.PdfSaveOptions saveOp = new com.aspose.diagram.PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.setWarningCallback(callback);



// pass the save options along with the save path to the save method.

diagram.save("C:\\temp\\Rendering.MissingFontNotification Out.pdf", saveOp);

{{< /highlight >}}
#### **تنفيذ IWarningCallback**
الخطوة الأخيرة هي إنشاء الفصل الذي يقوم بتطبيق[IWarning استدعاء](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)واجهه المستخدم. ستطبع هذه الفئة أي تحذيرات لاستبدال الخط بوحدة التحكم. يوضح المثال أدناه كيفية تنفيذ IWarningCallback ليتم إعلامك بأي استبدال للخط أثناء حفظ المستند.



**Java**

{{< highlight "java" >}}

 public class HandleDocumentWarnings implements IWarningCallback {

     /**

     * Our callback only needs to implement the "Warning" method. This method is

     * called whenever there is a potential issue during document processing.

     * The callback can be set to listen for warnings generated during document

     * load and/or document save.

     */

     public void warning(WarningInfo info) {

         // We are only interested in fonts being substituted.

         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION) {

         System.out.println("Font substitution: " + info.getDescription());

     }

 }

}

{{< /highlight >}}
