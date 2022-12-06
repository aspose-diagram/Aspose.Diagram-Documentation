---
title: Aspose.Diagram per Node.js tramite Java 22.5 Note di rilascio
type: docs
weight: 23
url: /it/java/aspose-diagram-for-node-js-via-java-22-5-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram per Node.js tramite Java 22.5.

{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50923|wk: campo Valori visualizzati|Aumento|
|DIAGRAMJAVA-50924|wk: ottiene i valori di allineamento|Aumento|
|DIAGRAMJAVA-50934|Indagare sulla fattibilità dell'elaborazione parallela dei file VSDX|Insetto|
|DIAGRAMJAVA-50936|Valori errati per Shape.getName(), Shape.getNameU()|Insetto|
|DIAGRAMJAVA-50941|Conversione da vsd a vsdx, il file vsdx convertito non può essere aperto in Visio.|Insetto|
|DIAGRAMJAVA-50942|Il valore di "ToSheet" viola la definizione di OpenXML nella conversione da vsd a vsdx.|Insetto|
|DIAGRAMJAVA-50943|Errore durante il caricamento del file VSD|Insetto|
|DIAGRAMJAVA-50951|Ridimensionamento della forma della linea laterale|Insetto|
|DIAGRAMJAVA-50955|Shape.getXForm().getWidth() restituisce un valore errato se la larghezza è impostata per utilizzare la formula|Insetto|

## `?`**Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.

### **Aggiunge getDisplayValue in Field**
- Ottiene il valore della stringa formattata di questo campo.

{{< highlight "java" >}}
String str = shape.getFields().get(0).getDisplayValue();
System.out.println(str);
{{< /highlight >}}

### **Aggiunge getInheritParas in Shape**
- Contiene i paragrafi per la forma ereditata dallo stile genitore e dal master

{{< highlight "java" >}}
int str = shape.getInheritParas().get(0).getHorzAlign().getValue();
System.out.println(str);
{{< /highlight >}}
