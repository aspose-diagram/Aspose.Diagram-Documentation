---
title: Lavorare con intestazioni e piè di pagina
type: docs
weight: 150
url: /it/java/working-with-headers-and-footers/
---
{{% alert color="primary" %}} 

Aspose.Diagram for Java fornisce un meccanismo per impostare intestazioni e piè di pagina dei diagrammi Microsoft Office Visio. Gli sviluppatori possono ottenere o impostare la stringa di testo che appare a sinistra, al centro ea destra dell'intestazione/piè di pagina di un documento. Possono anche impostare il margine dell'intestazione e del piè di pagina insieme alle proprietà del carattere del testo.

{{% /alert %}} 
### **Impostazione delle proprietà di intestazioni e piè di pagina**
 Il[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)L'oggetto class offre la proprietà HeaderFooter che consente di ottenere e impostare i valori di testo, carattere e margine di intestazione e piè di pagina. Durante l'anteprima di stampa del disegno Visio, gli utenti possono fare clic sul pulsante di collegamento "Modifica intestazione e piè di pagina" in Microsoft Visio 2013 (in Microsoft Visio 2010 >> pulsante "Intestazione e piè di pagina"). Ci sono alcune opzioni per aggiungere testo come mostrato nello screenshot qui sotto. Gli utenti possono gestire queste proprietà a livello di codice utilizzando Aspose.Diagram API come segue:

**Gestisci il testo di intestazioni e piè di pagina, i margini e le proprietà dei caratteri.** 

![cose da fare:immagine_alt_testo](working-with-headers-and-footers_1.png)

Il seguente pezzo di codice aiuta a gestire le proprietà di intestazioni e piè di pagina.
#### **Esempi di programmazione**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ManageHeadersandFooters.class);
// call the diagram constructor to a load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// add page number at the right corner of header
diagram.getHeaderFooter().setHeaderRight("&p");

// set text at the center
diagram.getHeaderFooter().setHeaderCenter("Center of the header");

// set text at the left side
diagram.getHeaderFooter().setHeaderLeft("Left of the header");

// add text at the right corner of footer
diagram.getHeaderFooter().setFooterRight("Right of the footer");

// set text at the center
diagram.getHeaderFooter().setFooterCenter("Center of the footer");

// set text at the left side
diagram.getHeaderFooter().setFooterLeft("Left of the footer");

// set header & footer color
diagram.getHeaderFooter().setHeaderFooterColor(Color.getRed());

// set text font properties
diagram.getHeaderFooter().getHeaderFooterFont().setItalic(BOOL.TRUE);
diagram.getHeaderFooter().getHeaderFooterFont().setUnderline(BOOL.FALSE);

// save Visio diagram
diagram.save(dataDir + "EditConnectorGeometry_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
