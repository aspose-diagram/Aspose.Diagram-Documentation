---
title: Aspose.Diagram for Java Note sulla versione 17.12
type: docs
weight: 10
url: /it/java/aspose-diagram-for-java-17-12-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for Java 17.12](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-12-release-notes/).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50290|Provide the single API to convert a Visio shape to PDF|Aumento|
|DIAGRAMJAVA-50291|Provide the single API to convert a Visio shape to HTML|Aumento|
|DIAGRAMJAVA-50572|Il metodo Shape.connectedShapes non recupera i nodi in uscita|Aumento|
|DIAGRAMJAVA-50391|The flipped images and arrows are generated on converting a VSD to SVG|Insetto|
|DIAGRAMJAVA-50570|VSD to PDF - the additional text items are added|Insetto|
|DIAGRAMJAVA-50571|Importa VSDX: si è verificato un errore nell'elemento forma|Insetto|
|DIAGRAMJAVA-50573|VSD to SVG - the lines of a group shape are missing|Insetto|
|DIAGRAMJAVA-50575|VSD to SVG - the text items are missing|Insetto|
|DIAGRAMJAVA-50576|La procedura di importazione VDX genera un errore dell'elemento della pagina|Insetto|
### **Aggiunge il membro Copy nella classe Shape**
Il membro copia accetta un'istanza di forma di destinazione, come parametro per clonare questa forma.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
### **Aggiunge il membro toPdf nella classe Shape**
The toPdf member converts a shape into the PDF format.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Aggiunge al membro HTML nella classe Shape**
The toHTML member converts a shape into the PDF format.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Copia una forma Visio in un'altra istanza di forma](https://docs.aspose.com/diagram/java/working-with-visio-shape-data/#use-connection-indexes-to-connect-shapes-programming-sample)
1. [Convert Visio Shape to PDF](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-pdf/)
1. [Convert Visio Shape to HTML](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-html/)


