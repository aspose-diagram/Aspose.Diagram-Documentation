---
title: Manage VBA codes of Visio Macro-Enabled diagram.
linktitle: Diagram VBA Project
type: docs
weight: 200
url: /net/working-with-vbaproject/

description: Add VBA Module and Modify VBA or Macro with Aspose.Diagram library.
---

## **Add a VBA Module**
{{% alert color="primary" %}}

Aspose.Diagram allows you to add a new VBA Module and Macro Code using Aspose.Diagram. Please use the [**Diagram.VbaProject.Modules.Add()**](https://apireference.aspose.com/diagram/net/aspose.diagram.vba/vbamodulecollection/methods/add/index) method to add the new VBA Module inside the diagram

{{% /alert %}}

The following sample code adds a new VBA Module and Macro Code and saves the output in the VSDM format. Once, you will open the output VSDM file in Microsoft Visio and click the **Developer > Visual Basic** menu commands, you will see a module named "TestModule" and inside it, you will see the following macro code.

{{< highlight java >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

Here is the sample code to generate the output VSDM file with VBA Module and Macro Code.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Vba-AddModule.cs" >}}

## **Modify VBA or Macro**

{{% alert color="primary" %}} 

You can modify VBA or Macro Code using Aspose.Diagram. Aspose.Diagram has added the following namespace and classes to read and modify the VBA project in the Visio file.

- Aspose.Diagram.Vba
- VbaProject
- VbaModuleCollection
- VbaModule

This article will show you how to change the VBA or Macro Code inside the source Visio file using Aspose.Diagram.

{{% /alert %}} 

The following sample code loads the source Visio file which has a following VBA or Macro code inside it

{{< highlight java >}}

 Sub Button1_Click()

    MsgBox "This is test message."

End Sub

{{< /highlight >}}

After the execution of Aspose.Diagram sample code, the VBA or Macro code will be modified like this

{{< highlight java >}}

 Sub Button1_Click()

    MsgBox "This is Aspose.Diagram message."

End Sub

{{< /highlight >}}

You can download the [source Visio file](1.vsdm) and the [output Visio file](1out.vsdm) from the given links.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Vba-ModifyModule.cs" >}}

## **Advance topics**
- [Check if Digital Signature of VBA Code is Valid](/diagram/net/check-if-digital-signature-of-vba-code-is-valid/)
- [Check if VBA Code is Signed](/diagram/net/check-if-vba-code-is-signed/)
- [Check if VBA Project is Protected and Locked for Viewing](/diagram/net/check-if-vba-project-is-protected-and-locked-for-viewing/)
- [Find out if VBA Project is Protected](/diagram/net/find-out-if-vba-project-is-protected/)