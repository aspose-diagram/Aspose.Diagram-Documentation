---
title: Convert Diagram Using LowCode API
linktitle: Diagram Converter
description: Demonstrates how to use Aspose.Diagram LowCode APIs to convert Diagram.
keywords: Aspose.Diagram, LowCode API, Diagram converter, convert Diagram, conversion between different visio file formats
type: docs
weight: 200
url: /net/convert-diagram-using-lowcode-api/
---

## **Introduction**
Aspose.Diagram for .NET provides the [Aspose.Diagram.LowCode] namespace, which simplifies common diagram processing tasks. This API is designed for developers who want to accomplish high‑level operations such as PDF conversion, diagram conversion with minimal effort.

The LowCode API is ideal for scenarios where quick implementation is more important than fine‑grained control. Aspose.Diagram LowCode APIs provide a high‑level, declarative way to perform common diagram tasks (conversion) without writing extensive boiler‑plate code. Let’s take a closer look at the LowCode capabilities of Aspose.Diagram for .NET.

## **Convert a diagram – DiagramConverter**

If you want to convert a diagram to other formats, you can use the **DiagramConverter** class to perform the conversion without writing extensive boiler‑plate code. The following code demonstrates how to convert an VSDX file ([lowcode-converter.vsdx](lowcode-converter.vsdx)) to VSDX format using the LowCode API.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
            
// Load a source Visio
Aspose.Diagram.LowCode.LowCodeLoadOptions loadOptions = new Aspose.Diagram.LowCode.LowCodeLoadOptions();
loadOptions.InputFile = dataDir + "Input.vsdx";
// Create save options with output file
Aspose.Diagram.LowCode.LowCodeSaveOptions saveOptions = new Aspose.Diagram.LowCode.LowCodeSaveOptions();

saveOptions.SaveFormat = SaveFileFormat.Vsdx;
saveOptions.OutputFile = "output.vsdx";
//Execute conversion
DiagramConverter.Process(loadOptions, saveOptions);

{{< /highlight >}}
```

## **Convert a Diagram – DiagramConverter & LowCodeLoadOptions & LowCodeSaveOptions**

If you want to convert a diagram to other formats, you can use the **DiagramConverter** class to perform the conversion without writing extensive boiler‑plate code. **LowCodeLoadOptions** and **LowCodeSaveOptions** let you fine‑tune the conversion behavior. The following code demonstrates how to convert an VSDX file ([lowcode-converter.vsdx](lowcode-converter.vsdx)) to VSDX format using **DiagramConverter**, **LowCodeLoadOptions**, and **LowCodeSaveOptions**.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
            
// Load a source Visio
Aspose.Diagram.LowCode.LowCodeLoadOptions loadOptions = new Aspose.Diagram.LowCode.LowCodeLoadOptions();
loadOptions.InputFile = dataDir + "Input.vsdx";
// Create save options with output file
Aspose.Diagram.LowCode.LowCodeSaveOptions saveOptions = new Aspose.Diagram.LowCode.LowCodeSaveOptions();

saveOptions.SaveFormat = SaveFileFormat.Vsdx;
saveOptions.OutputFile = "output.vsdx";
//Execute conversion
DiagramConverter.Process(loadOptions, saveOptions);

{{< /highlight >}}
```
