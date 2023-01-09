---
title: Aspose.Diagram for Java 17.8 Note di rilascio
type: docs
weight: 50
url: /it/java/aspose-diagram-for-java-17-8-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for Java 17.8](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-8-release-notes/).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMJAVA-50412|Missing shapes on converting a VST to PNG.|Insetto|
|DIAGRAMJAVA-50497|Uscita VSDX - disposizione errata di tutte le linee di collegamento.|Insetto|
|DIAGRAMJAVA-50500|Output VSDX: la dimensione della forma aggiunta manualmente non viene modificata.|Insetto|
|DIAGRAMJAVA-50511|Output VSDX - testo fuori posizione del connettore dinamico.|Insetto|
|DIAGRAMJAVA-50516|Output VSDX - la linea di collegamento che passa attraverso un'altra forma.|Insetto|
|DIAGRAMJAVA-50517|Output VSDX - la forma della decisione sta diventando più grande.|Insetto|
|DIAGRAMJAVA-50520|Impossibile impostare il comportamento di sovrapposizione delle linee di collegamento in un disegno VSDX.|Insetto|
|DIAGRAMJAVA-50521|Uscita VSDX - disposizione errata della linea del connettore.|Insetto|
|DIAGRAMJAVA-50522|Output PNG - the text of shape goes out of the boundary.|Insetto|
|DIAGRAMJAVA-50523|Uscita VSDX - disposizione errata della linea di collegamento.|Insetto|
|DIAGRAMJAVA-50525|Output VSDX - la formula della larghezza di qualsiasi forma non viene conservata.|Insetto|
|DIAGRAMJAVA-50528|Output VSDX - dimensione errata della forma.|Insetto|
|DIAGRAMJAVA-50529|Output VSDX - conserva le formule della sezione Trasformazione testo.|Insetto|
|DIAGRAMJAVA-50531|Output VSDX - il layout delle forme non è conforme alla larghezza e all'altezza nel foglio di forma.|Insetto|
|DIAGRAMJAVA-50533|Uscita VSDX - disposizione errata della linea di collegamento.|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Consulta l'elenco per eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. Se hai dubbi su qualsiasi modifica elencata, segnalala sul[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
### **Aggiunge un membro Quality nella classe SVGSaveOptions**
Ottiene o imposta un valore che determina la qualità delle immagini generate.

{{< highlight "java" >}}

 String dataDir = "c:\\temp\\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify SVG export settings

SVGSaveOptions options = new SVGSaveOptions();

// set image quality

options.setQuality(100);

// save drawing in the SVG format

diagram.save(dataDir + "UseSVGSaveOptions_out.svg", options);

{{< /highlight >}}
### **Aggiunge il metodo connectShapesViaConnectorIndex nella classe Page**
Permette di collegare le forme utilizzando gli indici di connessione.

{{< highlight "java" >}}

 String dataDir = "c:\\temp\\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shapes by ID

Shape shape1 = diagram.getPages().get(0).getShapes().getShape(1);

Shape shape2 = diagram.getPages().get(0).getShapes().getShape(2);

// add connector shapes

Shape connector1 = new Shape();

long connecter1Id = diagram.addShape(connector1, "Dynamic connector", 0);

// connect shapes by index of conneecting points

diagram.getPages().get(0).connectShapesViaConnectorIndex(shape1.getID(), 6, shape2.getID(), 3, connecter1Id);

// save drawing

diagram.save(dataDir + "UseSVGSaveOptions_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

1. [Usa gli indici di connessione per connettere le forme](https://docs.aspose.com/diagram/java/working-with-visio-shape-data/#use-connection-indexes-to-connect-shapes-programming-sample)
1. [Uso delle opzioni di salvataggio SVG](https://docs.aspose.com/diagram/java/save-visio-document/#use-of-the-svg-save-options)
