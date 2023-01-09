---
title: Stoppen Sie die Konvertierung oder das Laden mit InterruptMonitor, wenn es zu lange dauert
type: docs
weight: 30
url: /de/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **Mögliche Nutzungsszenarien**

Aspose.Diagram allows you to stop the conversion of Diagram to various formats like PDF, HTML etc. using the [**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) Objekt, wenn es zu lange dauert. Der Konvertierungsprozess ist häufig sowohl CPU- als auch speicherintensiv und es ist oft sinnvoll, ihn anzuhalten, wenn die Ressourcen begrenzt sind. Sie können verwenden[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) Sowohl zum Stoppen der Konvertierung als auch zum Stoppen des Ladens riesige diagram. Bitte verwenden[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) Eigenschaft zum Stoppen der Konvertierung und[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) Grundstück zum Laden riesig diagram.

## **Stoppen Sie die Konvertierung oder das Laden mit InterruptMonitor, wenn es zu lange dauert**

Der folgende Beispielcode erläutert die Verwendung von[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) object. The code converts quite a large Visio file to PDF. It will take several seconds (i.e. *mehr als 30 Sekunden*), um es aufgrund dieser Codezeilen konvertieren zu lassen.

{{< highlight "java" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Wie du siehst**Riesig.vsdx** ist eine ziemlich große VSDX-Datei. Allerdings ist die**StopConversionOrLoadingUsingInterruptMonitor()**Methode unterbricht die Konvertierung nach 10 Sekunden und Programm endet/beendet. Bitte verwenden Sie den folgenden Code, um den Beispielcode auszuführen.

{{< highlight "java" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Beispielcode**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-StopConversionOrLoadingUsingInterruptMonitor.java" >}}
