---
title: Working with Diagram Using LowCode API
linktitle: Low Code
description: Demonstrates how to use Aspose.Diagram LowCode APIs to convert diagram to PDF, and diagram.Includes complete C# examples for PdfConverter, and DiagramConverter.
keywords: Aspose.Diagram, LowCode API, Diagram conversion,Visio, PDF, C#, .NET
type: docs
weight: 200
url: /net/work-with-diagram-using-lowcode-api/
---

## **Introduction**
Aspose.Diagram for .NET provides the [Aspose.Diagram.LowCode](https://reference.aspose.com/diagram/net/aspose.diagram.lowcode/) namespace, which simplifies common diagram processing tasks. This API is designed for developers who want to accomplish high‑level operations such as PDF conversion, diagram conversion with minimal effort.

The LowCode API is ideal for scenarios where quick implementation is more important than fine‑grained control. Aspose.Diagram LowCode APIs provide a high‑level, declarative way to perform common Diagram tasks (conversion) without writing extensive boiler‑plate code. Let’s take a closer look at the LowCode capabilities of Aspose.Diagram for .NET.

## **Available Features in LowCode API**
The Aspose.Diagram.LowCode namespace currently supports:

1. Converter for converting a template file to PDF.  
2. Converter for conversion between different diagram file formats, such as VSD, VSDX, VSTM, VDX, and so on.  

## **How to Use LowCode API**
Aspose.Diagramm LowCode APIs provide a high‑level, declarative way to perform common diagram tasks (conversion) without writing extensive boiler‑plate code.

### **Convert a Diagram to PDF – PdfConverter**

The [PdfConverter](https://reference.aspose.com/diagram/net/aspose.diagram.lowcode/pdfconverter/) class converts a template file to a PDF file. The following code demonstrates how to convert a diagram to PDF using [PdfConverter](https://reference.aspose.com/diagram/net/aspose.diagram.lowcode/pdfconverter/).


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
            
// Load a source Visio
Aspose.Diagram.LowCode.LowCodeLoadOptions loadOptions = new Aspose.Diagram.LowCode.LowCodeLoadOptions();
loadOptions.InputFile = dataDir + "Input.vsdx";
// Create save options with output file
Aspose.Diagram.LowCode.LowCodeSaveOptions saveOptions = new Aspose.Diagram.LowCode.LowCodeSaveOptions();

saveOptions.OutputFile = "output.pdf";
//Execute conversion
Aspose.Diagram.LowCode.PdfConverter.Process(loadOptions, saveOptions);

{{< /highlight >}}


### **Convert diagram file formats  – DiagramConverter**

The [DiagramConverter](https://reference.aspose.com/diagram/net/aspose.diagram.lowcode/diagramconverter/) class converts a given template file between diagram files and other formats. The following code demonstrates how to convert a diagram to other formats using [DiagramConverter](https://reference.aspose.com/diagram/net/aspose.diagram.lowcode/diagramconverter/).


{{< highlight csharp >}}
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


## **Why Use Aspose.Diagram Low Code**

The Aspose.Diagram.LowCode namespace helps you implement high‑level diagram processing tasks quickly with conversion. It is especially useful for developers who need speed, simplicity, and maintainable code when working with diagram.

To explore more advanced options, you can always combine LowCode APIs with the full Aspose.Diagram object model. See more Low‑Code examples in the [API documentation](https://reference.aspose.com/diagram/net/aspose.diagram.lowcode/).
