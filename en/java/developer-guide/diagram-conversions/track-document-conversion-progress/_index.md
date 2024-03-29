---
title: Track Document Conversion Progress
type: docs
weight: 970
url: /java/track-document-conversion-progress/
description: This section explains how to track conversion progress of visio files with Aspose.Diagram.
---

## **Possible Usage Scenarios**

Sometimes converting large visio files can take some time. During this time, you might want to show the document conversion progress instead of just a loading screen to enhance the usability of your application. Aspose.Diagram supports tracking document conversion process by providing the IPageSavingCallback interface. The IPageSavingCallback interface provides PageStartSaving and PageEndSaving methods that you can implement in your custom class. You may also control which pages are rendered as demonstrated in the T*estDiagramPageSavingCallback* custom class.

## **Track Document Conversion Progress**

The following code sample loads the [source visio file](Drawing1.vsdx) and prints its conversion progress in the console by using the *TestPageSavingCallback* custom class that implements the IPageSavingCallback interface.

## **Sample Code**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}

The following is the code for the *TestDiagramPageSavingCallback* custom class.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}

## **Console Output**

Start saving page index 0 of pages 11</br>
End saving page index 0 of pages 11</br>
Start saving page index 1 of pages 11</br>
End saving page index 1 of pages 11</br>
Start saving page index 2 of pages 11</br>
End saving page index 2 of pages 11</br>
Start saving page index 3 of pages 11</br>
End saving page index 3 of pages 11</br>
Start saving page index 4 of pages 11</br>
End saving page index 4 of pages 11</br>
Start saving page index 5 of pages 11</br>
End saving page index 5 of pages 11</br>
Start saving page index 6 of pages 11</br>
End saving page index 6 of pages 11</br>
Start saving page index 7 of pages 11</br>
End saving page index 7 of pages 11</br>
Start saving page index 8 of pages 11</br>
End saving page index 8 of pages 11
