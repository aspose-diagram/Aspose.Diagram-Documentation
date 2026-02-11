---
title: قم بإدارة رموز VBA الخاصة بـ Visio Macro-Enabled diagram.
linktitle: Diagram مشروع VBA
type: docs
weight: 200
url: /ar/net/working-with-vbaproject/
description: إضافة وحدة VBA النمطية وتعديل VBA أو ماكرو مع مكتبة Aspose.Diagram.
---
## **أضف وحدة VBA النمطية**
{{% alert color="primary" %}}

 يسمح لك Aspose.Diagram بإضافة وحدة جديدة لـ VBA وكود ماكرو باستخدام Aspose.Diagram. الرجاء استخدام[**Diagram.VbaProject.Modules.Add ()**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbamodulecollection/methods/add/index) طريقة لإضافة وحدة VBA الجديدة داخل diagram

{{% /alert %}}

 يضيف نموذج التعليمات البرمجية التالي وحدة VBA النمطية الجديدة ورمز الماكرو ويحفظ الإخراج بتنسيق VSDM. بمجرد فتح ملف الإخراج VSDM في Microsoft Visio والنقر فوق الزر**المطور> Visual Basic** أوامر القائمة ، سترى وحدة تسمى "TestModule" وداخلها ، سترى رمز الماكرو التالي.

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

فيما يلي نموذج التعليمات البرمجية لإنشاء ملف الإخراج VSDM باستخدام وحدة VBA وكود الماكرو.


{{< highlight csharp >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Add module
int index = diagram.VbaProject.Modules.Add(VbaModuleType.Procedural, "TestModule");
//Get module 
Aspose.Diagram.Vba.VbaModule module = diagram.VbaProject.Modules[index];
//Set module
module.Codes = "Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"Welcome to Aspose!\"\r\n\r\nEnd Sub\r\n";

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


## **تعديل VBA أو ماكرو**

{{% alert color="primary" %}} 

يمكنك تعديل VBA أو Macro Code باستخدام Aspose.Diagram. قام Aspose.Diagram بإضافة مساحة الاسم والفئات التالية لقراءة وتعديل مشروع VBA في ملف Visio.

- Aspose.Diagram.Vba
- VbaProject
- مجموعة VbaModuleCollection
- VbaModule

ستوضح لك هذه المقالة كيفية تغيير VBA أو Macro Code داخل الملف المصدر Visio باستخدام Aspose.Diagram.

{{% /alert %}} 

يقوم نموذج التعليمات البرمجية التالي بتحميل الملف المصدر Visio الذي يحتوي على رمز VBA أو Macro التالي بداخله

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is test message."

End Sub

{{< /highlight >}}

بعد تنفيذ رمز عينة Aspose.Diagram ، سيتم تعديل رمز VBA أو ماكرو بهذا الشكل

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is Aspose.Diagram message."

End Sub

{{< /highlight >}}

 يمكنك تنزيل ملف[المصدر Visio ملف]() و ال[ملف الإخراج Visio]() من الروابط المعطاة.


{{< highlight csharp >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Get module 
Aspose.Diagram.Vba.VbaModule module = diagram.VbaProject.Modules[2];
//Set module
module.Codes = "Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"This is Aspose.Diagram message.\"\r\n\r\nEnd Sub\r\n";

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


## **موضوعات مسبقة**
- [تحقق مما إذا كان رمز VBA قد تم توقيعه](/diagram/ar/net/check-if-vba-code-is-signed/)
