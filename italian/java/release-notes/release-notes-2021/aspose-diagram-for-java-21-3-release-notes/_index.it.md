---
title: Aspose.Diagram for Java 21.3 Note di rilascio
type: docs
weight: 10
url: /it/java/aspose-diagram-for-java-21-3-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for Java 21.3.

{{% /alert %}}
## **Miglioramenti e modifiche**  ##

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50711|NullPointerException genera quando si tenta di salvare il documento VDX come PNG|Aumento|
|DIAGRAMJAVA-50713|Problema di sovrapposizione del testo durante la conversione di VSDX in PDF|Aumento|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.
### **Aggiunto ConnectShapesViaConnector nella pagina**
- Connetti le forme tramite connettore.

{{< highlight "java" >}}

page.connectShapesViaConnector(id, "Port7", id, "Port21", id);

{{< /highlight >}}
### **Aggiunge GlueShapeToConnectorBeginX nella pagina**
- Incolla la forma usando BeginX



{{< highlight "java" >}}

page.glueShapeToConnectorBeginX(id, "Port7", id);

{{< /highlight >}}
### **Aggiunge GlueShapeToConnectorEndX nella pagina**
- Incolla la forma usando BeginX



{{< highlight "java" >}}

page.glueShapeToConnectorEndX(id, "Port21", id);

{{< /highlight >}}
### **Aggiunge CenterDrawing in Page**
- Centra le forme di una pagina rispetto all'estensione della pagina.



{{< highlight "java" >}}

page.centerDrawing();

{{< /highlight >}}
### **Aggiunge IsContain in Shape**
- Indica se questa forma contiene un'altra forma.



{{< highlight "java" >}}

OLE_Shape.isContain(shape)

{{< /highlight >}}