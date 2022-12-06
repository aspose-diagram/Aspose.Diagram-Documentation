---
title: Stoppen Sie die Konvertierung oder das Laden mit InterruptMonitor, wenn es zu lange dauert
type: docs
weight: 30
url: /de/net/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
description: In diesem Abschnitt wird erläutert, wie Sie die Konvertierung oder das Laden mit Aspose.Diagram stoppen.
---
## **Mögliche Nutzungsszenarien**

Mit Aspose.Diagram können Sie die Konvertierung von Diagram in verschiedene Formate wie PDF, HTML usw. stoppen, indem Sie die verwenden[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) Objekt, wenn es zu lange dauert. Der Konvertierungsprozess ist häufig sowohl CPU- als auch speicherintensiv und es ist oft sinnvoll, ihn anzuhalten, wenn die Ressourcen begrenzt sind. Sie können verwenden[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) Sowohl zum Stoppen der Konvertierung als auch zum Stoppen des Ladens riesige diagram. Bitte verwenden[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/interruptmonitor) Eigenschaft zum Stoppen der Konvertierung und[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/loadoptions/properties/interruptmonitor) Grundstück zum Laden riesig diagram.

## **Stoppen Sie die Konvertierung oder das Laden mit InterruptMonitor, wenn es zu lange dauert**

Der folgende Beispielcode erläutert die Verwendung von[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) Objekt. Der Code konvertiert eine ziemlich große Visio-Datei in PDF. Es dauert einige Sekunden (z*mehr als 30 Sekunden*), um es aufgrund dieser Codezeilen konvertieren zu lassen.

{{< highlight "csharp" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Wie du siehst**Riesig.vsdx** ist eine ziemlich große VSDX-Datei. Allerdings ist die**WaitForWhileAndThenInterrupt()**Methode unterbricht die Konvertierung nach 1 Sekunde und Programm endet/beendet. Bitte verwenden Sie den folgenden Code, um den Beispielcode auszuführen.

{{< highlight "csharp" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Beispielcode**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Interrupt-Interrupt-StopConversionOrLoadingUsingInterruptMonitor.cs" >}}
