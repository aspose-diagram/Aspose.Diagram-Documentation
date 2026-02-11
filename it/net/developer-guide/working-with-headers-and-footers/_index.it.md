---
title: Lavorare con intestazioni e piè di pagina
type: docs
weight: 140
url: /it/net/working-with-headers-and-footers/
description: Questa sezione spiega come impostare intestazioni e piè di pagina di Microsoft Office Visio con Aspose.Diagram.
---
## **Gestisci intestazioni e piè di pagina dei diagrammi Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) fornisce un meccanismo per impostare intestazioni e piè di pagina dei diagrammi Microsoft Office Visio. Gli sviluppatori possono ottenere o impostare la stringa di testo che appare a sinistra, al centro ea destra dell'intestazione/piè di pagina di un documento. Possono anche impostare il margine dell'intestazione e del piè di pagina insieme alle proprietà del carattere del testo.
### **Impostazione delle proprietà di intestazioni e piè di pagina**
 Il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)L'oggetto class offre la proprietà HeaderFooter che consente di ottenere e impostare i valori di testo, carattere e margine di intestazione e piè di pagina. Durante l'anteprima di stampa del disegno Visio, gli utenti possono fare clic sul pulsante di collegamento "Modifica intestazione e piè di pagina" in Microsoft Visio 2013 (in Microsoft Visio 2010 >> pulsante "Intestazione e piè di pagina"). Ci sono alcune opzioni per aggiungere testo come mostrato nello screenshot qui sotto. Gli utenti possono gestire queste proprietà a livello di codice utilizzando Aspose.Diagram API come segue:
#### **Esempio di programmazione**
Il seguente pezzo di codice aiuta a gestire le proprietà di intestazioni e piè di pagina.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_HeadersAndFooters();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add page number at the right corner of header
diagram.HeaderFooter.HeaderRight = "&p";

// Set text at the center
diagram.HeaderFooter.HeaderCenter = "Center of the header";

// Set text at the left side
diagram.HeaderFooter.HeaderLeft = "Left of the header";

// Add text at the right corner of footer
diagram.HeaderFooter.FooterRight = "Right of the footer";

// Set text at the center
diagram.HeaderFooter.FooterCenter = "Center of the footer";

// Set text at the left side
diagram.HeaderFooter.FooterLeft = "Left of the footer";

// Set header & footer color
diagram.HeaderFooter.HeaderFooterColor = Color.AliceBlue;

// Set text font properties
diagram.HeaderFooter.HeaderFooterFont.Italic = BOOL.True;
diagram.HeaderFooter.HeaderFooterFont.Underline = BOOL.False;

// Save Visio diagram
diagram.Save(dataDir + "ManageHeadersandFooters_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

