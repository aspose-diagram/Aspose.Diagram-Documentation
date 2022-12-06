---
title: Detenga la conversión o la carga con InterruptMonitor cuando tarde demasiado
type: docs
weight: 30
url: /es/net/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
description: Esta sección explica cómo detener la conversión o la carga con Aspose.Diagram.
---
## **Posibles escenarios de uso**

Aspose.Diagram le permite detener la conversión de Diagram a varios formatos como PDF, HTML, etc. usando el[**InterrumpirMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) objeto cuando está tardando demasiado. El proceso de conversión suele hacer un uso intensivo de la CPU y la memoria y suele ser útil detenerlo cuando los recursos son limitados. Puedes usar[**InterrumpirMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) tanto para detener la conversión como para detener la carga enorme diagram. Utilice[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/interruptmonitor) propiedad para detener la conversión y[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/loadoptions/properties/interruptmonitor) propiedad para carga enorme diagram.

## **Detenga la conversión o la carga con InterruptMonitor cuando tarde demasiado**

El siguiente código de ejemplo explica el uso de[**InterrumpirMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) objeto. El código convierte un archivo Visio bastante grande a PDF. Tardará varios segundos (es decir,*más de 30 segundos*) para convertirlo debido a estas líneas de código.

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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Interrupt-Interrupt-StopConversionOrLoadingUsingInterruptMonitor.cs" >}}
