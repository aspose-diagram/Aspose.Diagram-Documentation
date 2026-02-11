---
title: Stoppen Sie die Konvertierung oder das Laden mit InterruptMonitor, wenn es zu lange dauert
type: docs
weight: 30
url: /de/net/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
description: In diesem Abschnitt wird erläutert, wie Sie die Konvertierung oder das Laden mit Aspose.Diagram stoppen.
---
## **Mögliche Nutzungsszenarien**

Aspose.Diagram allows you to stop the conversion of Diagram to various formats like PDF, HTML etc. using the [**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) Objekt, wenn es zu lange dauert. Der Konvertierungsprozess ist häufig sowohl CPU- als auch speicherintensiv und es ist oft sinnvoll, ihn anzuhalten, wenn die Ressourcen begrenzt sind. Sie können verwenden[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) Sowohl zum Stoppen der Konvertierung als auch zum Stoppen des Ladens riesige diagram. Bitte verwenden[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/interruptmonitor) Eigenschaft zum Stoppen der Konvertierung und[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/loadoptions/properties/interruptmonitor) Grundstück zum Laden riesig diagram.

## **Stoppen Sie die Konvertierung oder das Laden mit InterruptMonitor, wenn es zu lange dauert**

Der folgende Beispielcode erläutert die Verwendung von[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) object. The code converts quite a large Visio file to PDF. It will take several seconds (i.e. *mehr als 30 Sekunden*), um es aufgrund dieser Codezeilen konvertieren zu lassen.

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

