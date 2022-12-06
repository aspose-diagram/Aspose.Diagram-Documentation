---
title: Arrêtez la conversion ou le chargement à l'aide d'InterruptMonitor lorsque cela prend trop de temps
type: docs
weight: 30
url: /fr/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **Scénarios d'utilisation possibles**

Aspose.Diagram allows you to stop the conversion of Diagram to various formats like PDF, HTML etc. using the [**Moniteur d'interruption**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) objet quand cela prend trop de temps. Le processus de conversion est souvent gourmand en CPU et en mémoire et il est souvent utile de l'arrêter lorsque les ressources sont limitées. Vous pouvez utiliser[**Moniteur d'interruption**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) à la fois pour arrêter la conversion et pour arrêter le chargement de l'énorme diagram. Veuillez utiliser[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) propriété d'arrêter la conversion et[**LoadOptions.InterruptMonitorLoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) propriété pour le chargement énorme diagram.

## **Arrêtez la conversion ou le chargement à l'aide d'InterruptMonitor lorsque cela prend trop de temps**

L'exemple de code suivant explique l'utilisation de[**Moniteur d'interruption**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) object. The code converts quite a large Visio file to PDF. It will take several seconds (i.e. *plus de 30 secondes*) pour le convertir à cause de ces lignes de code.

{{< highlight "java" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Comme tu vois**énorme.vsdx** est un fichier VSDX assez énorme. Cependant, le**StopConversionOrLoadingUsingInterruptMonitor()**La méthode interrompt la conversion après 10 secondes et le programme se termine/se termine. Veuillez utiliser le code suivant pour exécuter l'exemple de code.

{{< highlight "java" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Exemple de code**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-StopConversionOrLoadingUsingInterruptMonitor.java" >}}
