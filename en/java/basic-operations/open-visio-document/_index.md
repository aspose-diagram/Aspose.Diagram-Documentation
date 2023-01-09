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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ReadVisioDiagram-ReadVisioDiagram.java" >}}
