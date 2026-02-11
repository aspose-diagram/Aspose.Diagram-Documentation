---
title: Detenga la conversión o la carga con InterruptMonitor cuando tarde demasiado
type: docs
weight: 30
url: /es/net/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
description: Esta sección explica cómo detener la conversión o la carga con Aspose.Diagram.
---
## **Posibles escenarios de uso**

Aspose.Diagram allows you to stop the conversion of Diagram to various formats like PDF, HTML etc. using the [**InterrumpirMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) objeto cuando está tardando demasiado. El proceso de conversión suele hacer un uso intensivo de la CPU y la memoria y suele ser útil detenerlo cuando los recursos son limitados. Puedes usar[**InterrumpirMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) tanto para detener la conversión como para detener la carga enorme diagram. Utilice[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/interruptmonitor) propiedad para detener la conversión y[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/loadoptions/properties/interruptmonitor) propiedad para carga enorme diagram.

## **Detenga la conversión o la carga con InterruptMonitor cuando tarde demasiado**

El siguiente código de ejemplo explica el uso de[**InterrumpirMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) object. The code converts quite a large Visio file to PDF. It will take several seconds (i.e. *más de 30 segundos*) para convertirlo debido a estas líneas de código.

{{< highlight "csharp" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Como ves**Enorme.vsdx** es un archivo VSDX bastante grande. sin embargo, el**WaitForWhileAndThenInterrupt()**El método interrumpe la conversión después de 1 segundo y el programa finaliza/finaliza. Utilice el siguiente código para ejecutar el código de muestra.

{{< highlight "csharp" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Código de muestra**
```
{{< highlight "csharp" >}}
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
```
