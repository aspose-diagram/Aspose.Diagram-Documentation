---
title: تحقق مما إذا كان رمز VBA قد تم توقيعه
type: docs
weight: 100
url: /ar/net/check-if-vba-code-is-signed/
description: تحقق مما إذا كان رمز vba موقعًا بمكتبة Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram يسمح للمستخدم بالتحقق مما إذا كان مشروع كود VBA موقعاً أم لا. الرجاء استخدام[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) للتحقق مما إذا كان مشروع رمز VBA موقّعًا أم لا.

{{% /alert %}}

 يشرح الكود التالي كيفية التحقق مما إذا كان رمز VBA موقّعًا أم لا يستخدم ملف[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) منشأه. يمكنك استخدام أي من ملفات visio الخاصة بك لاختبار هذا الرمز. لأغراض الاختبار ، يمكنك استخدام[هذا الملف visio المستخدم في الكود](1.vsdm).

## عينة من الرموز


{{< highlight csharp >}}

// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");

// Signature is valid
Console.WriteLine("Is VBA Code Project Signed: " + diagram.VbaProject.IsSigned);

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


## إخراج وحدة التحكم

 أدناه هو إخراج وحدة التحكم من الكود أعلاه باستخدام[عينة ملف visio](1out.vsdm) المقدمة من الرابط.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
