---
title: أدخل عنصر تحكم ActiveX في Visio Diagram
type: docs
weight: 10
url: /ar/java/insert-an-activex-control-in-the-visio-diagram/
---
{{% alert color="primary" %}}

 يمكن للمطورين إضافة عناصر تحكم ActiveX مباشرة إلى رسومات Microsoft Visio لجعل Visio diagram تفاعليًا باستخدام[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **أدخل نموذج برمجة عنصر تحكم ActiveX**
[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) تقدم class طريقة addActiveXControl وتسمح للمطورين بإدراج أي نوع من عناصر تحكم ActiveX مثل زر الأمر ومربع التحرير والسرد ومربع الاختيار ومربع القائمة ومربع النص وزر الدوران وزر الاختيار والتسمية والصورة وزر التبديل وشريط التمرير.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(InsertanActiveControl.class) + "VisioActiveXControls/";
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);
// Save diagram
diagram.save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

