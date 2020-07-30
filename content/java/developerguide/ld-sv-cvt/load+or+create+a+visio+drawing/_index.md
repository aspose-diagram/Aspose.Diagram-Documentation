---
title : "Load or Create a Visio Drawing" 
description : "" 
weight : 12018 
toc : false
type: docs
url: /java/developerguide/ld-sv-cvt/load+or+create+a+visio+drawing/
---

# Aspose.Diagram for Java : Load or Create a Visio Drawing


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Visio Diagram Load Overview](#visio-diagram-load-overview)
*   2 [Creating a New Visio Drawing](#creating-a-new-visio-drawing)
    *   2.1 [Create Visio Drawing Programming Sample](#create-visio-drawing-programming-sample)
*   3 [Read an Existing Visio Drawing](#read-an-existing-visio-drawing)
    *   3.1 [Reading a Diagram](#reading-a-diagram)
        *   3.1.1 [Reading Diagram Programming Sample](#reading-diagram-programming-sample)
{{< /panel >}}
 

 

## Visio Diagram Load Overview

The [Diagram](https://apireference.aspose.com/java/diagram/com.aspose.diagram/Diagram) class represents a Microsoft Office Visio diagram loaded into the memory. The `Diagram` class has several overloaded constructors allowing developers to create a blank drawing or to load one from a file or stream.

## Creating a New Visio Drawing

Aspose.Diagram for Java lets you read and create Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. The first step when creating new documents, is to create a diagram. Then add shapes and connectors to build up the diagram.

### Create Visio Drawing Programming Sample

The code below shows to create a new Microsoft Visio drawing. Please note that the blank drawing contains a single empty page.

The drawing paper size is Letter by default.

## Read an Existing Visio Drawing

Aspose.Diagram API supports creating the new Visio diagrams from the scratch and then save in any supported file format. Developers can also load an existing Visio diagram for the modification, addition or processing purposes.  

### Reading a Diagram

Using Aspose.Diagram API, developers can load all the supported Visio file formats. The available constructors of the Diagram class allow to do so and they accept a valid file path string or a file stream of the source Visio file.

The supported readable file formats are as follows:  
**VSDX, VSD, VSDM, VSS, VSSM, VSSX, VTX, VDX, VDW, VST, VSTX, VSTM and VSX**

Constructors of the diagram class also offer an optional parameter that defines `LoadFileFormat` or `LoadOptions`. It is the pre load information which developers can pass to the Aspose.Diagram API. We recommend passing the realistic information to get an ideal performance.

#### Reading Diagram Programming Sample

