---
title: Different Ways to Open Files
type: docs
weight: 10
url: /python-net/different-ways-to-open-files/
---

{{% alert color="primary" %}}

With Aspose.Diagram it is simple to open files, for example, to retrieve data, or to use a designer template to speed up the development process.

{{% /alert %}}

## **Opening a File via a Path**

Developers can open a Microsoft Diagram file using its file path on the local computer by specifying it in the **Diagram** class constructor. Simply pass the path in the constructor as a *string*. Aspose.Diagram will automatically detect the file format type.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaPath.py" >}}

## **Opening a File via a Stream**

It is also simple to open an Visio file as a stream. To do so, use an overloaded version of the constructor that takes the *BufferStream* object that contains the file.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaStream.py" >}}

## **Opening a File with LoadOptions**

To open a file with loadoptions, use the **LoadOptions** classes to set the related options of the classes for the template file to be loaded.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaLoadOptions.py" >}}

