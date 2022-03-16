---
title: Stop conversion or loading using InterruptMonitor when it is taking too long
type: docs
weight: 30
url: /java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---

## **Possible Usage Scenarios**

Aspose.Diagram allows you to stop the conversion of Diagram to various formats like PDF, HTML etc. using the [**InterruptMonitor**](https://apireference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) object when it is taking too long. The conversion process is often both CPU and Memory intensive and it is often useful to halt it when resources are limited. You can use [**InterruptMonitor**](https://apireference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) both for stopping conversion as well as to stop loading huge diagram. Please use [**Diagram.InterruptMonitor**](https://apireference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) property for stopping conversion and [**LoadOptions.InterruptMonitor**](https://apireference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) property for loading huge diagram.

## **Stop conversion or loading using InterruptMonitor when it is taking too long**

The following sample code explains the usage of [**InterruptMonitor**](https://apireference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) object. The code converts quite a large Visio file to PDF. It will take several seconds (i.e. *more than 30 seconds*) to get it converted because of these lines of code.

{{< highlight java >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

As you see **Huge.vsdx** is quite a huge VSDX file. However, the **StopConversionOrLoadingUsingInterruptMonitor()** method interrupts the conversion after 10 seconds and program ends/terminates. Please use the following code to execute the sample code.

{{< highlight java >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Sample Code**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-StopConversionOrLoadingUsingInterruptMonitor.java" >}}
