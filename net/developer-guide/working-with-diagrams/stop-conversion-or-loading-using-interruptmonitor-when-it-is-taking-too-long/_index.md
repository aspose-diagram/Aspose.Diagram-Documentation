---
title: Stop conversion or loading using InterruptMonitor when it is taking too long
type: docs
weight: 30
url: /net/
description: This section explains how to stop conversion or loading with Aspose.Diagram.
---

## **Possible Usage Scenarios**

Aspose.Diagram allows you to stop the conversion of Diagram to various formats like PDF, HTML etc. using the [**InterruptMonitor**](https://apireference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) object when it is taking too long. The conversion process is often both CPU and Memory intensive and it is often useful to halt it when resources are limited. You can use [**InterruptMonitor**](https://apireference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) both for stopping conversion as well as to stop loading huge diagram. Please use [**Diagram.InterruptMonitor**](https://apireference.aspose.com/diagram/net/aspose.diagram/diagram/properties/interruptmonitor) property for stopping conversion and [**LoadOptions.InterruptMonitor**](https://apireference.aspose.com/diagram/net/aspose.diagram/loadoptions/properties/interruptmonitor) property for loading huge diagram.

## **Stop conversion or loading using InterruptMonitor when it is taking too long**

The following sample code explains the usage of [**InterruptMonitor**](https://apireference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) object. The code converts quite a large Visio file to PDF. It will take several seconds (i.e. *more than 30 seconds*) to get it converted because of these lines of code.

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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Interrupt-Interrupt-StopConversionOrLoadingUsingInterruptMonitor.cs" >}}
