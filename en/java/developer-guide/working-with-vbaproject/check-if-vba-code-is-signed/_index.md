---
title: Check if VBA Code is Signed
type: docs
weight: 100
url: /java/check-if-vba-code-is-signed/
description: Check if the vba code is signed with Aspose.Diagram library.
---

{{% alert color="primary" %}}

Aspose.Diagram allows the user to check if the VBA code project is signed or not. Please use the [**Diagram.VbaProject.IsSigned**] property to check if the VBA code project is signed or not.

{{% /alert %}}

The following code explains how to check if the VBA code is signed or not using the [**Diagram.VbaProject.IsSigned**] property. You can use any of your visio files to test this code. For testing purposes, you can use [this visio file used in the code](1.vsdm).

## Sample Code

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
  
//Check signed     
boolean isSigned = diagram.getVbaProject().isSigned();

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## Console Output

Below is the console output of the above code using the [sample visio file](1out.vsdm) provided by the link.

{{< highlight java >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
