---
title: Aspose.Diagram for Java 20.5 Note di rilascio
type: docs
weight: 30
url: /it/java/aspose-diagram-for-java-20-5-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for Java 20.5.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50487|Displaced text items on converting a VSD to SVG|Aumento|
|DIAGRAMJAVA-50692|Bold text incorrectly positioned when saving VSDX as SVG|Aumento|
|DIAGRAMJAVA-50693|Images are not present in output SVG|Insetto|
|DIAGRAMJAVA-50695|Impossibile salvare il file VSDX come immagine: genera NullPointerException|Insetto|
## **Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram per JAVA. In caso di dubbi su qualsiasi modifica elencata, segnalarla al forum di supporto Aspose.Diagram.
### **Aggiunge isIntersect in Shape**
Indica se questa forma si interseca con un'altra forma.

{{< highlight "java" >}}

 boolean isIntersect = s1.isIntersect(s2);

{{< /highlight >}}
