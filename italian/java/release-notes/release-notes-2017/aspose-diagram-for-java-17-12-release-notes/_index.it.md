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
|DIAGRAMJAVA-50290|Fornisci il singolo API per convertire una forma Visio in PDF|Aumento|
|DIAGRAMJAVA-50291|Fornisci il singolo API per convertire una forma Visio in HTML|Aumento|
|DIAGRAMJAVA-50572|Il metodo Shape.connectedShapes non recupera i nodi in uscita|Aumento|
|DIAGRAMJAVA-50391|Le immagini e le frecce capovolte vengono generate durante la conversione di un VSD in SVG|Insetto|
|DIAGRAMJAVA-50570|VSD in PDF: vengono aggiunti gli elementi di testo aggiuntivi|Insetto|
|DIAGRAMJAVA-50571|Importa VSDX: si è verificato un errore nell'elemento forma|Insetto|
|DIAGRAMJAVA-50573|VSD a SVG - mancano le linee di una forma di gruppo|Insetto|
|DIAGRAMJAVA-50575|VSD in SVG: mancano gli elementi di testo|Insetto|
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
Il membro toPdf converte una forma nel formato PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Aggiunge al membro HTML nella classe Shape**
Il membro toHTML converte una forma nel formato PDF.

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
1. [Converti Visio Shape in PDF](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-pdf/)
1. [Converti la forma Visio in HTML](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-html/)


