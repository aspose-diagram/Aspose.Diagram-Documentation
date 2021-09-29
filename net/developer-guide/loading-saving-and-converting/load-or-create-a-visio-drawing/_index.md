---
title: Load or Create a Visio Drawing
type: docs
weight: 10
url: /net/load-or-create-a-visio-drawing/
---

## **Visio Diagram Load Overview**
The [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class represents a Microsoft Office Visio diagram loaded into the memory. The Diagram class has several overloaded constructors allowing developers to create a blank drawing or to load one from a file or stream.
## **Creating a New Visio Drawing**
Aspose.Diagram for .NET lets you read and create Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. The first step when creating new documents, is to create a diagram. Then add shapes and connectors to build up the diagram.
### **Create Visio Drawing Programming Sample**
The code below shows to create a new Microsoft Visio drawing. Please note that the blank drawing contains a single empty page.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-CreateNewVisio-CreateNewVisio.cs" >}}

{{% alert color="primary" %}} 

The drawing paper size is Letter by default.

{{% /alert %}} 
## **Read an Existing Visio Drawing**
Aspose.Diagram API supports creating the new Visio diagrams from the scratch and then save in any supported file format. Developers can also load an existing Visio diagram for the modification, addition or processing purposes.  
### **Reading a Diagram**
Using Aspose.Diagram API, developers can load all the supported Visio file formats. The available constructors of the Diagram class allow to do so and they accept a valid file path string or a file stream of the source Visio file.

The supported readable file formats are as follows:
**VSDX, VSD, VSDM, VSS, VSSX, VSSM, VTX, VSTM, VDX, VDW, VST, VSTX and VSX**

Constructors of the diagram class also offer an optional parameter that defines LoadFileFormat or LoadOptions. It is the pre load information which developers can pass to the Aspose.Diagram API. We recommend passing the realistic information to get an ideal performance.
#### **Reading Diagram Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ReadVisioDiagram-ReadVisioDiagram.cs" >}}
