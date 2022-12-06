---
title: Aspose.Diagram for Java 17.02.0 Note di rilascio
type: docs
weight: 110
url: /it/java/aspose-diagram-for-java-17-02-0-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.Diagram for Java 17.02.0](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-02-release-notes/).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50037|VSD to PDF conversion, the background color shade of a group shape is getting changed.|Insetto|
|DIAGRAMJAVA-50365|A blank page is generated while converting a Visio page with equations to PNG.|Insetto|
|DIAGRAMJAVA-50461|Borders are missing while converting VSDX to PNG.|Insetto|
|DIAGRAMJAVA-50462|Symbol disappears while converting VSDX to PNG.|Insetto|
|DIAGRAMJAVA-50463|Symbol disappears while converting VSDX to SVG.|Insetto|
|DIAGRAMJAVA-50465|Color of the text is different while converting VSDX to PNG.|Insetto|
|DIAGRAMJAVA-50466|The text position is incorrect when VSD is converted to SVG format.|Insetto|
|DIAGRAMJAVA-50237|` `[VSDX to PDF]- Error message occurred when used LeagueGothic Regular font.|Eccezione|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Consulta l'elenco per eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. Se hai dubbi su qualsiasi modifica elencata, segnalala sul[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge il metodo Shape.getParentShape**
Il metodo Shape.getParentShape permette di ottenere la forma genitore di una forma recente.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the Visio drawing

Diagram diagram = new Diagram("Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);

Shape parentShape = shape.getParentShape();

System.out.println("Parent Shape's Properties:");

System.out.println("Shape ID: " + parentShape.getID());

System.out.println("Shape Name: " + parentShape.getName());

System.out.println("Shape Type: " + parentShape.getType());

{{< /highlight >}}
### **Aggiunge il metodo Shape.isInGroup**
Il metodo Shape.isInGroup consente di rilevare se la forma recente fa parte di una qualsiasi forma di gruppo.

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the Visio drawing

Diagram diagram = new Diagram("Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);

System.out.println("Is it in a Group: " + shape.isInGroup());

{{< /highlight >}}
### **Aggiunge la classe misurata**
Viene aggiunta la classe Metered. Consente agli sviluppatori di sbloccare i limiti di valutazione di Aspose.Diagram API nonché di tenere traccia e mantenere le licenze API. Monitora anche l'uso regolare di Aspose.Diagram API.

{{< highlight "java" >}}

 // Initialize a Metered license class object

Metered metered = new Metered();

// apply public and private keys

metered.setMeteredKey("your-public-key", "your-private-key");

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Impostare le chiavi pubbliche e private per applicare la licenza misurata](/diagram/it/java/licensing/#licensing-setpublicandprivatekeystoapplymeteredlicense)
1. [Recupera la forma padre di una forma secondaria](/diagram/it/java/add-retrieve-copy-and-read-visio-shape-data/#add-retrieve-copyandreadvisioshapedata-retrievetheparentshapeofasub-shape)
1. [Verificare se la forma Visio si trova in un gruppo di forme](https://docs.aspose.com/diagram/java/group-convert-and-verify-shapes/)


