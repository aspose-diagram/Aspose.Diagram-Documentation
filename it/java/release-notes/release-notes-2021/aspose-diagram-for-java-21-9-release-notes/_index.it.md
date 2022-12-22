---
title: Aspose.Diagram for Java 21.9 Note di rilascio
type: docs
weight: 4
url: /it/java/aspose-diagram-for-java-21-9-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for Java 21.9.

{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50753|wk: controlla se TextAnnotation è connesso alla forma|Aumento|
|DIAGRAMJAVA-50382|The shading of shapes is missing on converting a VSDX to PDF|Insetto|
|DIAGRAMJAVA-50754|wk - LineColor da InheritLine non è corretto|Insetto|
|DIAGRAMJAVA-50756|wk: PinPos null vs centro-centro|Insetto|
|DIAGRAMJAVA-50757|WK: valore getBegin/End Arrow errato.|Insetto|
|DIAGRAMJAVA-50771|WK: impossibile ottenere LineColor e il nome per la forma del foglio|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.

### **Aggiunge dependOnShapes in Shape**
- Restituisce una matrice che contiene gli identificatori delle forme che dipendono da una forma.



{{< highlight "java" >}}

long[]shapeids = shape.dependsOnShapes();

{{< /highlight >}}
