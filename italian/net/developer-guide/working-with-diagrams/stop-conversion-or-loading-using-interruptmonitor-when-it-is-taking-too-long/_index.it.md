---
title: Interrompi la conversione o il caricamento utilizzando InterruptMonitor quando impiega troppo tempo
type: docs
weight: 30
url: /it/net/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
description: Questa sezione spiega come interrompere la conversione o il caricamento con Aspose.Diagram.
---
## **Possibili scenari di utilizzo**

Aspose.Diagram allows you to stop the conversion of Diagram to various formats like PDF, HTML etc. using the [**Monitor di interruzione**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) oggetto quando ci vuole troppo tempo. Il processo di conversione è spesso intensivo sia per la CPU che per la memoria ed è spesso utile interromperlo quando le risorse sono limitate. Puoi usare[**Monitor di interruzione**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) sia per interrompere la conversione che per interrompere il caricamento di enormi diagram. Si prega di utilizzare[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/interruptmonitor) proprietà per interrompere la conversione e[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/loadoptions/properties/interruptmonitor) proprietà per il caricamento enorme diagram.

## **Interrompi la conversione o il caricamento utilizzando InterruptMonitor quando impiega troppo tempo**

Il seguente codice di esempio spiega l'utilizzo di[**Monitor di interruzione**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) object. The code converts quite a large Visio file to PDF. It will take several seconds (i.e. *più di 30 secondi*) per convertirlo a causa di queste righe di codice.

{{< highlight "csharp" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Come vedi**Enorme.vsdx** è un file VSDX piuttosto grande. in ogni caso, il**WaitForWhileAndThenInterrupt()**Il metodo interrompe la conversione dopo 1 secondo e il programma termina/termina. Utilizzare il codice seguente per eseguire il codice di esempio.

{{< highlight "csharp" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Codice di esempio**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Interrupt-Interrupt-StopConversionOrLoadingUsingInterruptMonitor.cs" >}}
