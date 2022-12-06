---
title: Aspose.Diagram for Python via Java 22.11 Release Notes
type: docs
weight: 17
url: /it/python-java/aspose-diagram-for-python-via-java-22-11-release-notes/
---
{{% alert color="primary" %}}

This page contains release notes information for Aspose.Diagram for Python via Java 22.11.

{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-51049|Come ottenere il punto di connessione di una linea su una forma|Aumento|
|DIAGRAMJAVA-51044|.getDisplayText() per decodificare le entità html (file Aspose.Diagram Java 22.10, .vsd)|Aumento|
|DIAGRAMJAVA-51046|Il nome della forma a volte è diverso dai nomi in Visio|Insetto|

## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.

### **Aggiunge getConnectorRule in Shape**
- Restituisce un connectorRule che contiene l'id della forma e il connecton che sono connessi alla forma

{{< highlight "java" >}}
ConnectorRule rule= shape.getConnectorRule();
{{< /highlight >}}

### **Aggiunge setSavingCustomLinePattern in SVGSaveOptions**
- Definisce se salvare il modello di linea personalizzato.

{{< highlight "java" >}}
SVGSaveOptions saveOp = new SVGSaveOptions(); 
saveOp.setSavingCustomLinePattern(false);
{{< /highlight >}}
