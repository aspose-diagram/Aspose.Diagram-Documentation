---
title: Open Visio document programmatically
linktitle: Open Visio document
type: docs
weight: 20
url: /java/open-visio-document/
description: This page describes how to open Visio document from scratch with Aspose.Diagram library.
---

## **Read an Existing Visio Drawing**
Aspose.Diagram API supports creating the new Visio diagrams from the scratch and then save in any supported file format. Developers can also load an existing Visio diagram for the modification, addition or processing purposes.  
### **Reading a Diagram**
Using Aspose.Diagram API, developers can load all the supported Visio file formats. The available constructors of the Diagram class allow to do so and they accept a valid file path string or a file stream of the source Visio file.

The supported readable file formats are as follows:
**VSDX, VSD, VSDM, VSS, VSSM, VSSX, VTX, VDX, VDW, VST, VSTX, VSTM and VSX**

Constructors of the diagram class also offer an optional parameter that defines LoadFileFormat or LoadOptions. It is the pre load information which developers can pass to the Aspose.Diagram API. We recommend passing the realistic information to get an ideal performance.
#### **Reading Diagram Programming Sample**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadVisioDiagram.class);   
// Open the stream. Read only access is enough for Aspose.Diagram to load a diagram.
InputStream stream = new FileInputStream(dataDir + "Drawing1.vsdx");

//Call the diagram constructor to load diagram from a VSDX stream
Diagram vsdDiagram = new Diagram(stream);
stream.close();

//Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "Drawing1.vdx");

/*
 * Call diagram constructor to load diagram from a VSS file
 * providing load file format
*/
Diagram vssDiagram = new Diagram(dataDir + "Basic.vss", LoadFileFormat.VSS);

/*
 * Call diagram constructor to load diagram from a VSX file
 * providing load options
*/
LoadOptions loadOptions = new LoadOptions(LoadFileFormat.VSX);
Diagram vsxDiagram = new Diagram(dataDir + "Drawing1.vsx", loadOptions);

{{< /highlight >}}
```
