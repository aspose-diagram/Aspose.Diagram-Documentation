---
title: 当时间过长时使用 InterruptMonitor 停止转换或加载
type: docs
weight: 30
url: /zh/net/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
description: 本节介绍如何使用 Aspose.Diagram 停止转换或加载。
---
## **可能的使用场景**

Aspose.Diagram allows you to stop the conversion of Diagram to various formats like PDF, HTML etc. using the [**中断监视器**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor)反对时间太长。转换过程通常是 CPU 和内存密集型的，当资源有限时停止它通常很有用。您可以使用[**中断监视器**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor)既用于停止转换也用于停止加载巨大的 diagram。请使用[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/interruptmonitor)停止转换的属性和[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/loadoptions/properties/interruptmonitor)用于加载巨大 diagram 的属性。

## **当时间过长时使用 InterruptMonitor 停止转换或加载**

下面的示例代码解释了[**中断监视器**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) object. The code converts quite a large Visio file to PDF. It will take several seconds (i.e. *超过 30 秒*因为这些代码行而将其转换。

{{< highlight "csharp" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

正如你看到的**巨大.vsdx**是一个非常大的 VSDX 文件。但是，那**WaitForWhileAndThenInterrupt()**方法在 1 秒后中断转换，程序结束/终止。请使用以下代码来执行示例代码。

{{< highlight "csharp" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **示例代码**

{{< highlight csharp >}}
static string outputDir = RunExamples.Get_OutputDirectory();

//Create InterruptMonitor object
InterruptMonitor im = new InterruptMonitor();

//This function will load diagram
void loadDiagram()
{
    try
	  {
	
	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

	  }
	  catch(Exception e)
	  {
	      Console.WriteLine("Diagram Process Interrupted - Message: " + e.Message);
	  }

}

//This function will interrupt the conversion process after 1s
void WaitForWhileAndThenInterrupt()
{
    Thread.Sleep(1000 * 1);
    im.Interrupt();
}

public void TestRun()
{
    ThreadStart ts1 = new ThreadStart(this.loadDiagram);
    Thread t1 = new Thread(ts1);
    t1.Start();

    ThreadStart ts2 = new ThreadStart(this.WaitForWhileAndThenInterrupt);
    Thread t2 = new Thread(ts2);
    t2.Start();

    t1.Join();
    t2.Join();
}


public static void Run()
{
    new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

    Console.WriteLine("Interrupt successfully.");
}
{{< /highlight >}}

