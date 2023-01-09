---
title: Aspose.Diagram for Node.js via Java 21.12 Release Notes
type: docs
weight: 3
url: /it/java/aspose-diagram-for-node-js-via-java-21-12-release-notes/
---
{{% alert color="primary" %}}

This page contains release notes information for Aspose.Diagram for Node.js via Java 21.12.


{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50838|Centratura del testo sul connettore a linea retta|Insetto|
|DIAGRAMJAVA-50839|È necessario disegnare un connettore dritto tra le forme|Insetto|
## `?`**Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.


### **Aggiunge IsSavingImageSeparately in SVGSaveOptions**
- Definisce se salvare l'immagine separatamente.

{{< highlight "java" >}}

    SVGSaveOptions o = new SVGSaveOptions();
    o.setIsSavingImageSeparately(true);

{{< /highlight >}}


### **Aggiunge CustomImagePath in SVGSaveOptions**
- Il percorso personalizzato dell'utente (URL) salvato nel file svg generato per l'immagine. Se non definito dall'utente, verrà utilizzata la directory corrente.

{{< highlight "java" >}}

  o.setCustomImagePath("d:/output/");

{{< /highlight >}}

### **Aggiunge SaveForegroundPagesOnly in PrintSaveOptions**
- Specifica se verranno stampate tutte le pagine o solo in primo piano.

{{< highlight "java" >}}

 options.setSaveForegroundPagesOnly(true);

{{< /highlight >}}
