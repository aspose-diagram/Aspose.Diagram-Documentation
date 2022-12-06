---
title: Aspose.Diagram for Java 20.2 Note di rilascio
type: docs
weight: 60
url: /it/java/aspose-diagram-for-java-20-2-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for Java 20.2.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50361|The shape foreground color is not being preserved on converting a VST to PNG|Aumento|
|DIAGRAMJAVA-50504|VSD to PDF - the color of lines is changed|Aumento|
## ` `**Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.
### **Aggiunto enlargePage in ImageSaveOptions**
- Specifica se ingrandire la pagina

{{< highlight "java" >}}

 com.aspose.diagram.ImageSaveOptions o = new com.aspose.diagram.ImageSaveOptions(SaveFileFormat.PNG);

opt.setEnlargePage(false);

{{< /highlight >}}
### **Aggiunto hasHiddenInfo in Diagram**
- Indica se questo diagram ha informazioni nascoste

{{< highlight "java" >}}

 diagram.hasHiddenInfo();

{{< /highlight >}}




