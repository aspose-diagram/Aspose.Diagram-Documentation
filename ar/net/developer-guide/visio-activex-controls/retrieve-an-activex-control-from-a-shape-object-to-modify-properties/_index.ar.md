---
title: استرداد عنصر تحكم ActiveX من كائن الشكل لتعديل الخصائص
type: docs
weight: 20
url: /ar/net/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
description: تعديل خصائص عنصر تحكم activeX مع مكتبة Aspose.Diagram.
---
{{% alert color="primary" %}} 

باستخدام Aspose.Diagram API ، يمكن للمطورين استرداد عنصر تحكم ActiveX من كائن شكل Visio لتعيين جميع خصائصه المتاحة.

{{% /alert %}} 
## **استرجع عينة برمجة تحكم ActiveX**
[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) تقدم الفئة خاصية ActiveXControl التي تسمح للمطورين باسترداد عنصر تحكم ActiveX من كائن شكل Visio. يمكن للمطورين إرسال عنصر تحكم ActiveX في فئة عنصر تحكم ActiveX المناسبة ، ثم تعيين جميع خصائصه المتاحة.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioActiveXControls();
// Load and get a Visio page by name
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");            
Page page = diagram.Pages.GetPage("Page-1");
// Get a shape by ID
Shape shape = page.Shapes.GetShape(1);
// Get an ActiveX control
CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.ActiveXControl;
// Set width, height and caption of the command button control
cbac.Width = 4;           
cbac.Height = 4;           
cbac.Caption = "Test Button";
// Save diagram
diagram.Save(dataDir + "RetrieveActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
