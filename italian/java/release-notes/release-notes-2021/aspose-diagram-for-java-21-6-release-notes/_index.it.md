---
title: Aspose.Diagram for Java 21.6 Note di rilascio
type: docs
weight: 7
url: /it/java/aspose-diagram-for-java-21-6-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for Java 21.6.

{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50725|Arrotondamento degli angoli errato durante la conversione da vsdx a svg|Aumento|
|DIAGRAMJAVA-50724|Regressione in Aspose Diagram Java 21.3 - visualizzazione connettore errata|Insetto|
|DIAGRAMJAVA-50727|Workiva: ottenere i margini predefiniti del blocco di testo|Insetto|
|DIAGRAMJAVA-50728|Workiva: gradiente di colore di riempimento ereditato|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.
### **Aggiunge setEmfRenderSetting in SVGSaveOptions**
- Impostazione per il rendering del metafile EMF

{{< highlight "java" >}}
SVGSaveOptions saveOp = new SVGSaveOptions();          
saveOp.setEmfRenderSetting(EmfRenderSetting.EMF_PLUS_PREFER);

{{< /highlight >}}
### **Aggiunge getInheritTextBlock in Shape**
- Contiene i valori del blocco di testo per la forma ereditata dallo stile padre e dalla forma principale.

{{< highlight "java" >}}

 shape.getInheritTextBlock().getRightMargin().getValue()

{{< /highlight >}}
