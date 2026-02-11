---
title: استرداد عنصر تحكم ActiveX من كائن الشكل لتعديل الخصائص
type: docs
weight: 20
url: /ar/java/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
---
{{% alert color="primary" %}} 

باستخدام Aspose.Diagram API ، يمكن للمطورين استرداد عنصر تحكم ActiveX من كائن شكل Visio لتعيين جميع خصائصه المتاحة.

{{% /alert %}} 
## **استرجع عينة برمجة تحكم ActiveX**
[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) تقدم class طريقة getActiveXControl التي تسمح للمطورين باسترداد عنصر تحكم ActiveX من كائن شكل Visio. يمكن للمطورين إرسال عنصر تحكم ActiveX في فئة عنصر تحكم ActiveX المناسبة ، ثم تعيين جميع خصائصه المتاحة.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveActiveXControl.class) + "VisioActiveXControls/";
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");
// get a Visio page by name
Page page = diagram.getPages().getPage("Page-1");
// get a shape by ID
Shape shape = page.getShapes().getShape(1);
// get an ActiveX control
CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.getActiveXControl();
// set width of the command button control
cbac.setWidth(4);
// set height of the command button control
cbac.setHeight(4);
// set caption of the command button control
cbac.setCaption("Test Button");
// save diagram
diagram.save(dataDir + "RetrieveActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

