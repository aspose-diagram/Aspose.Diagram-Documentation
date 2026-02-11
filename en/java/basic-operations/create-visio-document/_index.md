---
title: Create Visio document programmatically
linktitle: Create Visio document
type: docs
weight: 10
url: /java/create-visio-document/
description: This page describes how to create Visio document from scratch with Aspose.Diagram library.
---


## **Creating a New Visio Drawing**
Aspose.Diagram for Java lets you read and create Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. The first step when creating new documents, is to create a diagram. Then add shapes and connectors to build up the diagram.
### **Create Visio Drawing Programming Sample**
The code below shows to create a new Microsoft Visio drawing. Please note that the blank drawing contains a single empty page.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

{{% alert color="primary" %}} 

The drawing paper size is Letter by default.

{{% /alert %}} 

