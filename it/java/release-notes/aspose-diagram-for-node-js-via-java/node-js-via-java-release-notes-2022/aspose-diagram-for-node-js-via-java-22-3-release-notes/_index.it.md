---
title: Aspose.Diagram for Node.js via Java 22.3 Release Notes
type: docs
weight: 25
url: /it/java/aspose-diagram-for-node-js-via-java-22-3-release-notes/
---
{{% alert color="primary" %}}

This page contains release notes information for Aspose.Diagram for Node.js via Java 22.3.

{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50883|Determina i caratteri mancanti e le informazioni sulla sostituzione dei caratteri da API|Insetto|

## `?`**Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.

### **Aggiunge AddText nella pagina**
- Aggiunge testo con PinX e PinY definiti.

{{< highlight "java" >}}
Shape shape = page.addText(1, 1, 2, 2, "Test text", "Calibri", "#a5a5a5", 0.25);
{{< /highlight >}}
