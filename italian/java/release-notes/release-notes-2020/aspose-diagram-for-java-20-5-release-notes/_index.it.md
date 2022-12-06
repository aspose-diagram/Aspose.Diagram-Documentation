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
|DIAGRAMJAVA-50487|Elementi di testo spostati durante la conversione di VSD in SVG|Aumento|
|DIAGRAMJAVA-50692|Testo in grassetto posizionato in modo errato durante il salvataggio di VSDX come SVG|Aumento|
|DIAGRAMJAVA-50693|Le immagini non sono presenti nell'output SVG|Insetto|
|DIAGRAMJAVA-50695|Impossibile salvare il file VSDX come immagine: genera NullPointerException|Insetto|
## **Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram per JAVA. In caso di dubbi su qualsiasi modifica elencata, segnalarla al forum di supporto Aspose.Diagram.
### **Aggiunge isIntersect in Shape**
Indica se questa forma si interseca con un'altra forma.

{{< highlight "java" >}}

 boolean isIntersect = s1.isIntersect(s2);

{{< /highlight >}}
