---
title: Aspose.Diagram per Python tramite Java 22.10 Note di rilascio
type: docs
weight: 18
url: /it/python-java/aspose-diagram-for-python-via-java-22-10-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram per Python tramite Java 22.10.

{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-51028|setTopPage non funziona|Aumento|
|DIAGRAMJAVA-51035|wk: la proprietà Geoms per alcune forme del foglio non viene risolta correttamente|Aumento|
|DIAGRAMJAVA-51030|.getName() a volte è diverso dai nomi nei file Visio (Aspose.Diagram Java 22.9, .vsd)|Insetto|
|DIAGRAMJAVA-51033|.getText() a volte è diverso da shape.Text in Visio (file Aspose.Diagram Java 22.9, .vsd)|Insetto|
|DIAGRAMJAVA-51038|Quando il testo contiene interruzioni di riga, il ricalcolo della larghezza del testo non è corretto|Insetto|
|DIAGRAMJAVA-51040|.getNameU() a volte è vuoto (file Aspose.Diagram Java 22.9, .vsd)|Insetto|

## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.

### **Aggiunge getDisplayText in Shape**
- Ottenere il testo visualizzato sull'interfaccia

{{< highlight "java" >}}
string text = shape.getDisplayText();
{{< /highlight >}}

### **Aggiunge getInheritGeoms in Shape**
- Contiene i valori Geoms per la forma ereditata dalla forma principale.

{{< highlight "java" >}}
int count = shape.getInheritGeoms().get(0).getCoordinateCol().getCount();
{{< /highlight >}}