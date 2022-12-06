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
|DIAGRAMJAVA-50097|Conversione da VSD a PDF - Le linee curve diventano una linea retta|Insetto|
|DIAGRAMJAVA-50161|Conversione da VTX a HTML - Manca l'immagine di sfondo dell'intero diagram|Insetto|
|DIAGRAMJAVA-50301|Esportazione da VSD a PDF: le forme di tipo Meta si trasformano in simboli disordinati|Insetto|
|DIAGRAMJAVA-50464|La forma è stata renderizzata in modo errato durante la conversione di VSDX in PNG|Insetto|
|DIAGRAMJAVA-50652|Da VISIO a PDF - Il PDF di output mostra un errore in Adobe Reader|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, segnalarli a il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge GetDefaultFontDir in Diagram**
Ottieni il percorso della cartella Font predefiniti

{{< highlight "java" >}}

  string str =  diagram.getDefaultFontDir();

{{< /highlight >}}
