---
title: Pubblico API Modifiche Aspose.Diagram 6.3.0
type: docs
weight: 30
url: /it/net/public-api-changes-in-aspose-diagram-6-3-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 6.0.0 alla 6.3.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
## **Rileva il formato di un file Visio**
**Vengono aggiunte varie classi, metodi e proprietà per rilevare il formato**
- **Aggiungere le classi FileFormatUtil e FileFormatInfo** 
 - Queste classi forniscono accesso programmatico per rilevare il tipo di file Visio.
- **Aggiunge il metodo DetectFileFormat nella classe FileFormatUtil** 
 - Rileva e restituisce le informazioni sul formato di un Visio diagram memorizzato in un file.
- **Aggiunge la proprietà FileFormatType nella classe FileFormatInfo** 
 - Ottiene il formato file rilevato.
- **Aggiunge la proprietà LoadFormat in FileFormatInfo** 
 - Ottiene il formato di caricamento rilevato.

 Gli sviluppatori possono facilmente rilevare il formato di qualsiasi file Visio. Questo argomento della guida illustra come rilevare il formato file Visio (utilizzando un percorso file o un flusso) e verificarne l'estensione:[Rileva il formato del file Visio](/diagram/it/net/introduction/#detect-the-format-of-visio-file)
## **Controlla l'esportazione di pagine nascoste Visio al salvataggio**
**Aggiunge la proprietà ExportHiddenPage nelle classi SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions e PdfSaveOptions**
- Definisce se è necessario esportare o meno le pagine Visio nascoste.

 Gli sviluppatori possono includere o escludere pagine Visio nascoste durante il salvataggio di un Visio diagram in file PDF, HTML, immagine (PNG, JPEG, GIF), SVG e XPS. Questo argomento della guida illustra come farlo:[Controlla l'esportazione di pagine nascoste Visio al salvataggio](/diagram/it/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
