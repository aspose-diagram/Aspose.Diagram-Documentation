---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /java/your-first-aspose-diagram-application-hello-world/
description: This page describes how to create first application with Aspose.Diagram library.
---

{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1. Create an instance of the [Diagram](https://apireference.aspose.com/diagram/java/com.aspose.diagram/diagram) class.
1. If you have a license, then [apply it](https://apireference.aspose.com/diagram/java/com.aspose.diagram/License).
   If you are using the evaluation version, skip the license related code lines.
1. Create a new Visio file, or open an existing Visio file.
1. Create a new text box.
1. Insert the words **Hello World!** into a text box.
1. Generate the modified Microsoft Visio file.

The implementation of the above steps is demonstrated in the examples below.

### **Code Sample: Creating a New Diagram**

The following example creates a new diagram from the scratch, writes Hello World! on the first page and saves the Visio file.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-CreateNewVisio-CreateNewVisio.java" >}}

### **Code Sample: Opening an Existing File**

The following example opens an existing Microsoft Visio template file named "Sample.vsdx", inputs "Hello World!" text in the first page and saves the diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ReadVisioDiagram-ReadVisioDiagram.java" >}}
