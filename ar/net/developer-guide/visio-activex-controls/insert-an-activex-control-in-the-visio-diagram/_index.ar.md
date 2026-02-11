---
title: أدخل عنصر تحكم ActiveX في Visio Diagram
type: docs
weight: 10
url: /ar/net/insert-an-activex-control-in-the-visio-diagram/
description: توضح هذه الصفحة كيفية إدراج عنصر تحكم activeX مع مكتبة Aspose.Diagram.
---
{{% alert color="primary" %}}

 يمكن للمطورين إضافة عناصر تحكم ActiveX مباشرة إلى رسومات Microsoft Visio لجعل Visio diagram تفاعليًا باستخدام[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **أدخل نموذج برمجة عنصر تحكم ActiveX**
[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) تقدم class طريقة AddActiveXControl وتسمح للمطورين بإدراج أي نوع من عناصر تحكم ActiveX مثل زر الأمر ومربع التحرير والسرد ومربع الاختيار ومربع القائمة ومربع النص وزر الدوران وزر الاختيار والتسمية والصورة وزر التبديل وشريط التمرير.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioActiveXControls();
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);
// Save diagram
diagram.Save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

