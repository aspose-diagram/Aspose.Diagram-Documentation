---
title: Hello World مثال
type: docs
weight: 100
url: /ar/java/hello-world-example/
---
## **Hello World مثال**
يتم استخدام مثال "Hello World" تقليديًا لإدخال ميزات لغة برمجة أو برنامج مع حالة استخدام بسيطة.

Aspose.Diagram for Java هو Visio معالجة ملفات API غنية بالمميزات تسمح لمطوري التطبيقات بتضمين Visio إنشاء مستندات وقراءتها وتحويلها في تطبيقاتهم Java. وهو يدعم العمل مع العديد من تنسيقات الملفات الشائعة Visio بما في ذلك VSDX و VDX و VSD و VSX و VTX و VSSX و VSDM و VSSM و VSTM و VDW و VSS و VST. تنسيقات مثل PDF و HTML و XML و SVG و XAML.

بعد، بعدما[تركيب Aspose.Diagram for Java](/diagram/ar/java/installation/)في بيئتك ، يمكنك تنفيذ نموذج التعليمات البرمجية أدناه لمعرفة كيفية عمل Aspose.Diagram API.

يتبع مقتطف الشفرة أدناه الخطوات التالية:

1. إنشاء كائن Diagram
1. استخدم طريقة Save لكائن فئة Diagram لحفظ الملف على القرص

مقتطف الكود التالي هو برنامج Hello World لعرض عمل Aspose.Diagram for Java API.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```




