---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /python-net/your-first-aspose-diagram-application-hello-world/
---

{{% alert color="primary" %}}

This beginner's topic shows how developers can create a simple first application (Hello World) using Aspose.Diagram' simple API. The application creates a Microsoft Visio file with the words Hello World in the page.

{{% /alert %}}

### **Creating the Hello World Application**

To create the Hello World application using Aspose.Diagram API:

1. Create an instance of the Workbook class.
1. Apply the license:
   1. If you have purchased a license, then use the license in your application to get access to Aspose.Diagram' full functionality
   1. If you are using the evaluation version of the component (if you're using Aspose.Diagram without a license), skip this step.
1. Create a new Microsoft Visio file, or open an existing file in which you want to add/update some text.
1. Insert the words **Hello World!** into the page accessed.
1. Generate the modified Microsoft Visio file.

The examples below demonstrate the above steps.

#### **Creating a Diagram**

The following example creates a new diagram from scratch, writes the words "Hello World!" on the first page, and saves the file.

**Create new visio file** 

![todo:image_alt_text](your-first-aspose-diagram-application-hello-world_1.png)

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingNewVisioFile.py" >}}

#### **Opening an Existing File**

The following example opens an existing Microsoft Visio template file, writes the words "Hello World!" in the first page, and saves the diagram as a new file.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingHelloWorldVisioFile.py" >}}
