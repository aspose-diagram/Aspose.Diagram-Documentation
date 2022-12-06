---
title: Stoppa konvertering eller laddning med InterruptMonitor när det tar för lång tid
type: docs
weight: 30
url: /sv/net/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
description: Det här avsnittet förklarar hur du stoppar konvertering eller laddning med Aspose.Diagram.
---
## **Möjliga användningsscenarier**

Aspose.Diagram låter dig stoppa konverteringen av Diagram till olika format som PDF, HTML etc. med hjälp av[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) objekt när det tar för lång tid. Konverteringsprocessen är ofta både CPU- och minnesintensiv och det är ofta användbart att stoppa den när resurserna är begränsade. Du kan använda[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) både för att stoppa konverteringen och för att sluta ladda enorma diagram. Använd[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/interruptmonitor) egendom för att stoppa konvertering och[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/loadoptions/properties/interruptmonitor) egendom för lastning av enorma diagram.

## **Stoppa konvertering eller laddning med InterruptMonitor när det tar för lång tid**

Följande exempelkod förklarar användningen av[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) objekt. Koden konverterar en ganska stor Visio-fil till PDF. Det tar flera sekunder (dvs*mer än 30 sekunder*) för att få det konverterat på grund av dessa kodrader.

{{< highlight "csharp" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Som du ser**Enorma.vsdx** är en ganska stor VSDX-fil. Men den**WaitForWhileAndThenInterrupt()**metoden avbryter konverteringen efter 1 sekund och programmet avslutas/avslutas. Använd följande kod för att köra exempelkoden.

{{< highlight "csharp" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Exempelkod**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Interrupt-Interrupt-StopConversionOrLoadingUsingInterruptMonitor.cs" >}}
