---
title: تحقق مما إذا كان رمز VBA قد تم توقيعه
type: docs
weight: 100
url: /ar/java/check-if-vba-code-is-signed/
description: تحقق مما إذا كان رمز vba موقعًا بمكتبة Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram يسمح للمستخدم بالتحقق مما إذا كان مشروع كود VBA موقعاً أم لا. الرجاء استخدام خاصية [** Diagram.VbaProject.IsSigned **] للتحقق مما إذا كان مشروع رمز VBA موقّعًا أم لا.

{{% /alert %}}

 يشرح الكود التالي كيفية التحقق مما إذا كان رمز VBA موقّعًا أم لا باستخدام خاصية [** Diagram.VbaProject.IsSigned **]. يمكنك استخدام أي من ملفات visio الخاصة بك لاختبار هذا الرمز. لأغراض الاختبار ، يمكنك استخدام[هذا الملف visio المستخدم في الكود](1.vsdm).

## عينة من الرموز

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
  
//Check signed     
boolean isSigned = diagram.getVbaProject().isSigned();

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## إخراج وحدة التحكم

 أدناه هو إخراج وحدة التحكم من الكود أعلاه باستخدام[عينة ملف visio](1out.vsdm) المقدمة من الرابط.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
