---
title: Insert an ActiveX Control in the Visio Diagram
type: docs
weight: 10
url: /net/insert-an-activex-control-in-the-visio-diagram/
description: This page describes how to insert an activeX Control with Aspose.Diagram library.
---

{{% alert color="primary" %}}

Developers can add ActiveX controls directly to Microsoft Visio drawings to make the Visio diagram interactive by using [Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Insert an ActiveX Control Programming Sample**
[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class offers AddActiveXControl method and allows developers to insert any type of ActiveX control like command button, combobox, checkbox, listbox, textbox, spin button, radio button, label, image, toggle button and scrollbar.

```
{{< highlight "csharp" >}}
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
```
