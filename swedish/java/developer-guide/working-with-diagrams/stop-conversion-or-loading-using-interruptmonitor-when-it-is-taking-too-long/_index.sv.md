---
title: Stoppa konvertering eller laddning med InterruptMonitor när det tar för lång tid
type: docs
weight: 30
url: /sv/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **Möjliga användningsscenarier**

Aspose.Diagram låter dig stoppa konverteringen av Diagram till olika format som PDF, HTML etc. med hjälp av[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) objekt när det tar för lång tid. Konverteringsprocessen är ofta både CPU- och minnesintensiv och det är ofta användbart att stoppa den när resurserna är begränsade. Du kan använda[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) både för att stoppa konverteringen och för att sluta ladda enorma diagram. Använd[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) egendom för att stoppa konvertering och[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) egendom för lastning av enorma diagram.

## **Stoppa konvertering eller laddning med InterruptMonitor när det tar för lång tid**

Följande exempelkod förklarar användningen av[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) objekt. Koden konverterar en ganska stor Visio-fil till PDF. Det tar flera sekunder (dvs*mer än 30 sekunder*) för att få det konverterat på grund av dessa kodrader.

{{< highlight "java" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Som du ser**Enorma.vsdx** är en ganska stor VSDX-fil. Men den**StopConversionOrLoadingUsingInterruptMonitor()**metoden avbryter konverteringen efter 10 sekunder och programmet avslutas/avslutas. Använd följande kod för att köra exempelkoden.

{{< highlight "java" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Exempelkod**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-StopConversionOrLoadingUsingInterruptMonitor.java" >}}
