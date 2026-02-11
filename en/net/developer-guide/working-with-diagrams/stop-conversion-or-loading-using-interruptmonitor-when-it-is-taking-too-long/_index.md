---
title: Stop conversion or loading using InterruptMonitor when it is taking too long
type: docs
weight: 30
url: /net/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
description: This section explains how to stop conversion or loading with Aspose.Diagram.
---

## **Possible Usage Scenarios**

Aspose.Diagram allows you to stop the conversion of Diagram to various formats like PDF, HTML etc. using the [**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) object when it is taking too long. The conversion process is often both CPU and Memory intensive and it is often useful to halt it when resources are limited. You can use [**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) both for stopping conversion as well as to stop loading huge diagram. Please use [**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/interruptmonitor) property for stopping conversion and [**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/loadoptions/properties/interruptmonitor) property for loading huge diagram.

## **Stop conversion or loading using InterruptMonitor when it is taking too long**

The following sample code explains the usage of [**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) object. The code converts quite a large Visio file to PDF. It will take several seconds (i.e. *more than 30 seconds*) to get it converted because of these lines of code.

{{< highlight csharp >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

As you see **Huge.vsdx** is quite a huge VSDX file. However, the **WaitForWhileAndThenInterrupt()** method interrupts the conversion after 1 seconds and program ends/terminates. Please use the following code to execute the sample code.

{{< highlight csharp >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Sample Code**

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

