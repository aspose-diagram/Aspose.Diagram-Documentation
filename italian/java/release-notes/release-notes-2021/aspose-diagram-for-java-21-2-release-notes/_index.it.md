---
title: Aspose.Diagram for Java 21.2 Note di rilascio
type: docs
weight: 11
url: /it/java/aspose-diagram-for-java-21-2-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for Java 21.2.

{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50710|aggiungi una singola riga a un file Viso, in modo che rimanga modificabile come una riga|Aumento|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.
### **Aggiunge activePage in Diagram**
- Specifica la pagina attiva

{{< highlight "java" >}}

 Page page = diagram.getActivePage()

{{< /highlight >}}
### **Aggiunge centerDrawing in Shape**
- Centrare la forma rispetto all'estensione della pagina

{{< highlight "java" >}}

 shape.centerDrawing()

{{< /highlight >}}
### **Aggiunge drawLine in Page**
- Il processo di tracciare una singola linea.

{{< highlight "java" >}}

  diagram.getPages().get(0).drawLine(0, 0, 1, 1);

{{< /highlight >}}