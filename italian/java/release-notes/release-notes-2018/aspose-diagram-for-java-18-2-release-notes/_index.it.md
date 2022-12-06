---
title: Aspose.Diagram for Java 18.2 Note di rilascio
type: docs
weight: 110
url: /it/java/aspose-diagram-for-java-18-2-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for Java 18.2](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-2-release-notes/).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50587|Aggiunto il supporto per il recupero dell'elemento Char relativo della parte di testo|Aumento|
|DIAGRAMJAVA-50478|Le linee del connettore passano attraverso le altre forme durante la conversione da VDX a VSDM|Insetto|
|DIAGRAMJAVA-50581|VSDX in PDF - resa errata delle sagome|Insetto|
|DIAGRAMJAVA-50582|Uscita VSDX - le linee di collegamento non sono diritte|Insetto|
|DIAGRAMJAVA-50583|VSD import: si è verificato un errore nell'elemento VisioDocument|Insetto|
|DIAGRAMJAVA-50584|VDX import: si è verificato un errore nell'elemento VisioDocument|Insetto|
|DIAGRAMJAVA-50585|VSD import: si è verificato un errore nell'elemento VisioDocument|Insetto|
|DIAGRAMJAVA-50586|VSDX a SVG - colore del bordo errato della forma|Insetto|
### **Aggiunge il metodo getInheritChars nella classe Shape**
Contiene i valori dei caratteri per la forma ereditata dalla forma master.

{{< highlight "java" >}}

 CharCollection charCollection = shape.getInheritChars();

{{< /highlight >}}
