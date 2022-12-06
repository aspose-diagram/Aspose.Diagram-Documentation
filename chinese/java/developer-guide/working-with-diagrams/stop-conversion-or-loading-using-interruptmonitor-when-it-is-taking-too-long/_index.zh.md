---
title: 当时间过长时使用 InterruptMonitor 停止转换或加载
type: docs
weight: 30
url: /zh/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **可能的使用场景**

Aspose.Diagram 允许您停止将 Diagram 转换为各种格式，如 PDF、HTML 等，使用[**中断监视器**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor)反对时间太长。转换过程通常是 CPU 和内存密集型的，当资源有限时停止它通常很有用。您可以使用[**中断监视器**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor)既用于停止转换也用于停止加载巨大的 diagram。请使用[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor)停止转换的属性和[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor)用于加载巨大 diagram 的属性。

## **当时间过长时使用 InterruptMonitor 停止转换或加载**

下面的示例代码解释了[**中断监视器**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor)目的。该代码将相当大的 Visio 文件转换为 PDF。这将需要几秒钟（即*超过 30 秒*因为这些代码行而将其转换。

{{< highlight "java" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

正如你看到的**巨大.vsdx**是一个非常大的 VSDX 文件。但是，那**StopConversionOrLoadingUsingInterruptMonitor()**方法在 10 秒后中断转换，程序结束/终止。请使用以下代码来执行示例代码。

{{< highlight "java" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **示例代码**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-StopConversionOrLoadingUsingInterruptMonitor.java" >}}
