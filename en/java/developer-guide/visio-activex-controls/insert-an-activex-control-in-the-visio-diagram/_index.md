---
title: Insert an ActiveX Control in the Visio Diagram
type: docs
weight: 10
url: /java/insert-an-activex-control-in-the-visio-diagram/
---

{{% alert color="primary" %}}

Developers can add ActiveX controls directly to Microsoft Visio drawings to make the Visio diagram interactive by using [Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **Insert an ActiveX Control Programming Sample**
[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class offers addActiveXControl method and allows developers to insert any type of ActiveX control like command button, combobox, checkbox, listbox, textbox, spin button, radio button, label, image, toggle button and scrollbar.


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

