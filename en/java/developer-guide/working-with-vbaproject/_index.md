---
title: Manage VBA codes of Visio Macro-Enabled diagram.
linktitle: Diagram VBA Project
type: docs
weight: 200
url: /java/working-with-vbaproject/

description: Add VBA Module and Modify VBA or Macro with Aspose.Diagram library.
---

## **Add a VBA Module**
{{% alert color="primary" %}}

Aspose.Diagram allows you to add a new VBA Module and Macro Code using Aspose.Diagram. Please use the [**Diagram.VbaProject.Modules.Add()**] method to add the new VBA Module inside the diagram

{{% /alert %}}

The following sample code adds a new VBA Module and Macro Code and saves the output in the VSDM format. Once, you will open the output VSDM file in Microsoft Visio and click the **Developer > Visual Basic** menu commands, you will see a module named "TestModule" and inside it, you will see the following macro code.

{{< highlight java >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

Here is the sample code to generate the output VSDM file with VBA Module and Macro Code.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Add module
int index = diagram.getVbaProject().getModules().add(VbaModuleType.PROCEDURAL, "TestModule");
//Get module 
com.aspose.diagram.VbaModule module = diagram.getVbaProject().getModules().get(index);
//Set module
module.setCodes("Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"Welcome to Aspose!\"\r\n\r\nEnd Sub\r\n");

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

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

You can download the [source Visio file]() and the [output Visio file]() from the given links.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Get module 
com.aspose.diagram.VbaModule module = diagram.getVbaProject().getModules().get(2);
//Set module
module.setCodes("Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"This is Aspose.Diagram message.\"\r\n\r\nEnd Sub\r\n");

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## **Advance topics**
- [Check if VBA Code is Signed](/diagram/java/check-if-vba-code-is-signed/)