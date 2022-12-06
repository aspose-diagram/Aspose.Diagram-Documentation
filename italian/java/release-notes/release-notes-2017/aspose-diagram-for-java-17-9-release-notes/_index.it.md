---
title: Aspose.Diagram for Java 17.9 Note di rilascio
type: docs
weight: 40
url: /it/java/aspose-diagram-for-java-17-9-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for Java 17.9](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-9-release-notes/).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50485|Aggiungi il supporto delle forme di spaziatura automatica in Visio|Aumento|
|DIAGRAMJAVA-50521|Uscita VSDX - disposizione errata della linea del connettore|Insetto|
|DIAGRAMJAVA-50522|Output PNG: il testo della forma esce dal confine|Insetto|
|DIAGRAMJAVA-50527|Output VSDX - la linea di collegamento tocca il limite della forma|Insetto|
|DIAGRAMJAVA-50540|Uscita VSDX - disposizione errata delle linee di collegamento|Insetto|
|DIAGRAMJAVA-50543|Output VSDX - layout errato e testo fuori posto delle linee di collegamento|Insetto|
|DIAGRAMJAVA-50545|Output VSDX - Impossibile formulare la posizione del testo in forma|Insetto|
|DIAGRAMJAVA-50547|Output VSDX - impossibile impostare il valore della proprietà come String|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Consulta l'elenco per eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. Se hai dubbi su qualsiasi modifica elencata, segnalala sul[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge il membro autoSpaceShapes in Page**
Permette di aggiungere uno spazio automatico tra la raccolta di forme.

{{< highlight "java" >}}

 AutoSpaceOptions options = new AutoSpaceOptions();

diagram.getPages().getPage(0).autoSpaceShapes(diagram.getPages().getPage(0).getShapes(), options);

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Spaziatura automatica una raccolta di forme nella pagina Visio](/diagram/it/java/auto-space-a-collection-of-shapes-in-the-visio-page/)
