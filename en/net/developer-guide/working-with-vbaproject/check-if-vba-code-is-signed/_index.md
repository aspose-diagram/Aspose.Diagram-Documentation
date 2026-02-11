---
title: Check if VBA Code is Signed
type: docs
weight: 100
url: /net/check-if-vba-code-is-signed/
description: Check if the vba code is signed with Aspose.Diagram library.
---

{{% alert color="primary" %}}

Aspose.Diagram allows the user to check if the VBA code project is signed or not. Please use the [**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) property to check if the VBA code project is signed or not.

{{% /alert %}}

The following code explains how to check if the VBA code is signed or not using the [**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) property. You can use any of your visio files to test this code. For testing purposes, you can use [this visio file used in the code](1.vsdm).

## Sample Code

```
{{< highlight "csharp" >}}

// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");

// Signature is valid
Console.WriteLine("Is VBA Code Project Signed: " + diagram.VbaProject.IsSigned);

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## Console Output

Below is the console output of the above code using the [sample visio file](1out.vsdm) provided by the link.

{{< highlight java >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
