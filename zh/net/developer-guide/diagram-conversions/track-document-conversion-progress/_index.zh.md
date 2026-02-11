---
title: 跟踪文档转换进度
type: docs
weight: 970
url: /zh/net/track-document-conversion-progress/
description: 本节介绍如何使用 Aspose.Diagram 跟踪 visio 文件的转换进度。
---
## **可能的使用场景**

有时转换大型 visio 文件可能需要一些时间。在此期间，您可能希望显示文档转换进度而不仅仅是加载屏幕，以增强应用程序的可用性。 Aspose.Diagram 通过提供支持跟踪文档转换过程**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**界面。这**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**接口提供**[PageStartSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pagestartsaving)**和**[PageEndSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pageendsaving)**您可以在自定义类中实现的方法。您还可以控制呈现哪些页面，如 T 中所示*estDiagramPageSavingCallback*自定义类。

## **跟踪文档转换进度**

以下代码示例加载[源文件 visio](Drawing1.vsdx)并使用*测试页面保存回调*实现的自定义类**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**界面。

## **示例代码**


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


以下是代码*测试图页面保存回调*自定义类。


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


## **控制台输出**

开始保存第 11 页的第 0 页索引</br>
结束保存第 11 页的第 0 页索引</br>
开始保存第 11 页的第 1 页索引</br>
结束保存页面索引 1，共 11 页</br>
开始保存第 11 页的第 2 页索引</br>
结束保存第 11 页的第 2 页索引</br>
开始保存第 11 页的第 3 页索引</br>
结束保存第 11 页的第 3 页索引</br>
开始保存第 11 页的第 4 页索引</br>
结束保存页面索引 4，共 11 页</br>
开始保存第 11 页的第 5 页索引</br>
结束保存页面索引 5 of pages 11</br>
开始保存第 11 页的第 6 页索引</br>
结束保存页面索引 6 of pages 11</br>
开始保存第 11 页的第 7 页索引</br>
结束保存页面索引 7 of pages 11</br>
开始保存第 11 页的第 8 页索引</br>
结束保存页面索引 8，共 11 页
