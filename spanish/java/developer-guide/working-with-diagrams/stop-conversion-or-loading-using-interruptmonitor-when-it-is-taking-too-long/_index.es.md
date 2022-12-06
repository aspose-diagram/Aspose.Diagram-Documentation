---
title: Detenga la conversión o la carga con InterruptMonitor cuando tarde demasiado
type: docs
weight: 30
url: /es/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **Posibles escenarios de uso**

Aspose.Diagram allows you to stop the conversion of Diagram to various formats like PDF, HTML etc. using the [**InterrumpirMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) objeto cuando está tardando demasiado. El proceso de conversión suele hacer un uso intensivo de la CPU y la memoria y suele ser útil detenerlo cuando los recursos son limitados. Puedes usar[**InterrumpirMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) tanto para detener la conversión como para detener la carga enorme diagram. Utilice[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) propiedad para detener la conversión y[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) propiedad para carga enorme diagram.

## **Detenga la conversión o la carga con InterruptMonitor cuando tarde demasiado**

El siguiente código de ejemplo explica el uso de[**InterrumpirMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) object. The code converts quite a large Visio file to PDF. It will take several seconds (i.e. *más de 30 segundos*) para convertirlo debido a estas líneas de código.

{{< highlight "java" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Como ves**Enorme.vsdx** es un archivo VSDX bastante grande. sin embargo, el**StopConversionOrLoadingUsingInterruptMonitor()**El método interrumpe la conversión después de 10 segundos y el programa termina/finaliza. Utilice el siguiente código para ejecutar el código de muestra.

{{< highlight "java" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Código de muestra**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-StopConversionOrLoadingUsingInterruptMonitor.java" >}}
