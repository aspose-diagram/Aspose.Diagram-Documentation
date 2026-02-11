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

Följande exempelkod förklarar användningen av[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) objekt. Koden konverterar en ganska stor Visio-fil till PDF. Det tar flera sekunder (dvs.*mer än 30 sekunder*) för att få det konverterat på grund av dessa kodrader.

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

