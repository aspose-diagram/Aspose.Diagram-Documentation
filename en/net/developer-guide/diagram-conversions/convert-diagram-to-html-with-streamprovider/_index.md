---
title: Convert Diagram To Html With Streamprovider
type: docs
weight: 970
url: /net/convert-diagram-to-html-with-streamprovider/
description: This section explains how to convert Diagram To html With Streamprovider.
---

## **Possible Usage Scenarios**

When converting visio files which contain iamges and shapes to html files, we offen face the following two issues:

1.Where should we save the images and shapes when saving excel file to html stream.
2.Replace the default path with excepted path.

This article explains how to implement IStreamProvider interface for setting the HTMLSaveOptions.StreamProvider property. By implementing this interface, you will be able to save the created resources during HTML generation to your specific locations or memory streams.

This is the main code showing the usage of HTMLSaveOptions.StreamProvider property

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToHTMLWithStreamprovider.cs" >}}

Here is the code for ExportStreamProvider class which implements IStreamProvider interface used inside the above code.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportStreamProvider.cs" >}}


