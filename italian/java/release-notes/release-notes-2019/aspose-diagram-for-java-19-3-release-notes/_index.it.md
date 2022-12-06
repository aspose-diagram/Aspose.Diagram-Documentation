---
title: Aspose.Diagram for Java 19.3 Note di rilascio
type: docs
weight: 100
url: /it/java/aspose-diagram-for-java-19-3-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per Aspose.Diagram for Java 19.3

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50339|Aggiunto il supporto per il recupero delle directory dei font comuni sui sistemi operativi|Aumento|
|DIAGRAMJAVA-50097|VSD to PDF conversion - Curved lines become a straight line|Insetto|
|DIAGRAMJAVA-50161|VTX to HTML conversion - Background picture of the whole diagram is missing|Insetto|
|DIAGRAMJAVA-50301|VSD to PDF export - Meta type shapes turn into messy symbols|Insetto|
|DIAGRAMJAVA-50464|The shape has rendered incorrectly while converting VSDX to PNG|Insetto|
|DIAGRAMJAVA-50652|VISIO to PDF - Output PDF shows error in Adobe Reader|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, segnalarli a il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge GetDefaultFontDir in Diagram**
Ottieni il percorso della cartella Font predefiniti

{{< highlight "java" >}}

  string str =  diagram.getDefaultFontDir();

{{< /highlight >}}
