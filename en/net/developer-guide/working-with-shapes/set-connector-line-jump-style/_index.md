---
title: Setting Connector line jump style
type: docs
weight: 40
url: /net/set-connector-line-jump-style/
---

The code below shows how to:

1. Load a sample file.
1. Access a particular shape.
1. Set shape's Jump style.
## **Set shape's Jump style Programming Sample**
Use the following code in your .NET application to set shape's jump style using Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
            
// Load a source Visio
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");

//Get the connector
Shape shape = diagram.Pages[0].Shapes.GetShape(1);     

//Set Jump Value
shape.SetConnectorJumpValue(ConLineJumpCodeValue.Always,ConLineJumpStyleValue.Arc);

// Save the new Visio
newDiagram.Save(dataDir + "out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```