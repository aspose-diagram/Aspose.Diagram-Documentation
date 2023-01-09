﻿---
title: Aspose.Diagram for Java 22.6 Note di rilascio
type: docs
weight: 22
url: /it/java/aspose-diagram-for-java-22-6-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for Java 22.6.

{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50963|WK: Shape distorted after saving to PNG|Aumento|
|DIAGRAMJAVA-50967|Ridimensionamento della forma della linea laterale [Cont.]|Insetto|
|DIAGRAMJAVA-50972|API non analizza correttamente il file|Insetto|
|DIAGRAMJAVA-50974|Problema nell'aggiunta di un nuovo punto di connessione|Insetto|

## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.

### **Aggiunge risoluzione in HTMLSaveOptions**
- Ottiene o imposta la risoluzione per il codice HTML generato, in punti per pollice.

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.setResolution(96);
{{< /highlight >}}