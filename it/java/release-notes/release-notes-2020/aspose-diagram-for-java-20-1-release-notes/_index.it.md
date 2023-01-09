---
title: Aspose.Diagram for Java 20.1 Note di rilascio
type: docs
weight: 70
url: /it/java/aspose-diagram-for-java-20-1-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for Java 20.1.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50664|Gradient fill not supported in export to SVG|Aumento|
|DIAGRAMJAVA-50670|Consenti il caricamento dei font dalla memoria|Aumento|
|DIAGRAMJAVA-50681|API sta impiegando molto tempo per caricare il file diagram di grandi dimensioni|Aumento|
|DIAGRAMJAVA-50381|The network shapes are not being preserved on converting a VSDX to PDF|Insetto|
|DIAGRAMJAVA-50386|The images are turned upside down with color difference on converting a VSD to SVG|Insetto|
|DIAGRAMJAVA-50679|VSDX to PDF - Connectors are missing in output|Insetto|
|DIAGRAMJAVA-50680|Visio to PNG - Output images were cropped out|Insetto|
## **Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram per JAVA. In caso di dubbi su qualsiasi modifica elencata, segnalarla al forum di supporto Aspose.Diagram.

- Aggiunti getPages e setPages in Page - Specifica l'indice delle pagine da caricare.

{{< highlight "java" >}}

 LoadOptions options = new LoadOptions(LoadFileFormat.VSDX);

options.setPages(new ArrayList());

options.getPages().add(0);

{{< /highlight >}}

- Aggiunge setFontSources in FontConfigs: imposta le origini dei caratteri.

{{< highlight "java" >}}

 byte[]b = new byte[]{ 0 };

com.aspose.diagram.MemoryFontSource sc1 = new com.aspose.diagram.MemoryFontSource(b);

com.aspose.diagram.MemoryFontSource sc2 = new com.aspose.diagram.MemoryFontSource(b);

com.aspose.diagram.MemoryFontSource[]sc = new com.aspose.diagram.MemoryFontSource[]{ sc1, sc2 };

com.aspose.diagram.FontConfigs.setFontSources(sc); 

{{< /highlight >}}


