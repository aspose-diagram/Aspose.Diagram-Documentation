---
title: Track Document Conversion Progress
type: docs
weight: 970
url: /net/track-document-conversion-progress/
description: This section explains how to track conversion progress of visio files with Aspose.Diagram.
---

## **Possible Usage Scenarios**

Sometimes converting large visio files can take some time. During this time, you might want to show the document conversion progress instead of just a loading screen to enhance the usability of your application. Aspose.Diagram supports tracking document conversion process by providing the **[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)** interface. The **[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)** interface provides **[PageStartSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pagestartsaving)** and **[PageEndSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pageendsaving)** methods that you can implement in your custom class. You may also control which pages are rendered as demonstrated in the T*estDiagramPageSavingCallback* custom class.

## **Track Document Conversion Progress**

The following code sample loads the [source visio file](Drawing1.vsdx) and prints its conversion progress in the console by using the *TestPageSavingCallback* custom class that implements the **[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)** interface.

## **Sample Code**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance PDF save options class
Aspose.Diagram.Saving.PdfSaveOptions options = new Aspose.Diagram.Saving.PdfSaveOptions();
          
//set page saving call back
options.PageSavingCallback = new TestDiagramPageSavingCallback();

// save Visio drawing
diagram.Save(dataDir + "Callback_out.pdf", options);

{{< /highlight >}}


The following is the code for the *TestDiagramPageSavingCallback* custom class.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
public class TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback
{
    public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)
    {
        Console.WriteLine("Start saving diagram page index {0} of pages {1}", args.PageIndex, args.PageCount);
    }

    public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)
    {
        Console.WriteLine("End saving diagram page index {0} of pages {1}", args.PageIndex, args.PageCount);

        //don't output pages after page index 8.
        if (args.PageIndex >= 8)
        {
            args.HasMorePages = false;
        }
    }
}

{{< /highlight >}}


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
