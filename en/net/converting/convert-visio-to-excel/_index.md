---
title: Convert Visio to Excel format 
linktitle: Convert Visio to Excel
type: docs
weight: 9
url: /net/convert-visio-to-excel/
description: This topic show you how to Aspose.Diagram allows to convert Visio to Excel formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to CSV with a few lines of code.
---


## **Export to CSV**
{{% alert color="primary" %}}

Aspose.Diagram for .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to CSV, Aspose.Diagram for .NET populates **Application** field with value 'Aspose.Diagram' and **CSV Producer** field with value, e.g 'Aspose.Diagram 23.4'.

Please note that you cannot instruct Aspose.Diagram for .NET API to change or remove this information from output Documents.

{{% /alert %}}

This article explains how to export a Microsoft Visio diagram to CSV using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

Use the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class constructor to read the diagram files and the Save method to export the diagram to any supported image format.

To export VSD diagram to CSV:

1. Create an instance of the Diagram class.
1. Call the Diagram classs Save method and set the output format to CSV.

### **Export Microsoft Visio Drawing to CSV**
The code samples show how to export Microsoft Visio Drawing to CSV using C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToCSV.vsd");

MemoryStream csvStream = new MemoryStream();
// Save diagram
diagram.Save(csvStream, SaveFileFormat.CSV);

// Create a CSV file
FileStream csvFileStream = new FileStream(dataDir + "ExportToCSV_out.csv", FileMode.Create, FileAccess.Write);
csvFileStream.WriteTo(csvFileStream);
csvFileStream.Close();

csvFileStream.Close();

// Display Status.
System.Console.WriteLine("Conversion from vsd to csv performed successfully.");

{{< /highlight >}}
```

