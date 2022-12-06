---
title: Aspose.Diagram for .NET 6.3.0 Note di rilascio
type: docs
weight: 90
url: /it/net/aspose-diagram-for-net-6-3-0-release-notes/
---
## **Altri miglioramenti e modifiche**

|**Chiave** |**Riepilogo** |**Categoria** |
|:- |:- |:- |
|DIAGRAMNET-50739 | Aggiungere il supporto per il rilevamento del tipo Visio diagram.| Nuova caratteristica|
|DIAGRAMNET-50746 | Impedisci l'esportazione delle pagine Visio nascoste nel PDF.| Nuova caratteristica|
|DIAGRAMNET-50747 | Impedisci l'esportazione delle pagine Visio nascoste nell'HTML.| Nuova caratteristica|
|DIAGRAMNET-50750 | Impedisci l'esportazione delle pagine Visio nascoste nel PNG.| Nuova caratteristica|
|DIAGRAMNET-50751 | Impedisci l'esportazione delle pagine Visio nascoste nel JPEG.| Nuova caratteristica|
|DIAGRAMNET-50752 | Impedisci l'esportazione delle pagine Visio nascoste nell'SVG.| Nuova caratteristica|
|DIAGRAMNET-50753 | Impedisci l'esportazione delle pagine Visio nascoste nella GIF.| Nuova caratteristica|
|DIAGRAMNET-50754 | Impedisci l'esportazione delle pagine Visio nascoste nell'XPS.| Nuova caratteristica|
|DIAGRAMNET-50541 | VSDX alla conversione PDF, gli elementi di testo in ebraico vengono visualizzati in ordine inverso.| Aumento|
|DIAGRAMNET-50542 | Conversione da VSD a PDF, la parola araba si trasforma in lettere.| Aumento|
|DIAGRAMNET-50682 | VSD all'esportazione in PDF, il testo della cella della tabella è parzialmente invisibile.| Insetto|
|DIAGRAMNET-50712 | VDX in esportazione PDF: il testo di varie forme è fuori luogo.| Insetto|
|DIAGRAMNET-50741 | VSD all'esportazione SVG mancano alcune forme Visio.| Insetto|
|DIAGRAMNET-50742 | VSD all'esportazione SVG non applica il colore bianco interno delle forme.| Insetto|
|DIAGRAMNET-50744 |La routine di apertura e salvataggio di VSDX ha modificato il testo in caratteri fittizi.| Insetto|
|DIAGRAMNET-50745 | La routine di apertura e salvataggio di VSDX ha modificato il formatore della linea tratteggiata.| Insetto|
|DIAGRAMNET-50748 | VSD in esportazione PDF: gli elementi di testo sono fuori posto.| Insetto|
|DIAGRAMNET-50763 | L'esportazione da VSD a VDX genera l'errore dell'elemento principale.| Insetto|
### **Pubblico API e modifiche incompatibili con le versioni precedenti**
Consulta l'elenco per eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. Se hai dubbi su qualsiasi modifica elencata, segnalala sul[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
#### **Aggiungere le classi FileFormatUtil e FileFormatInfo**
Queste classi forniscono l'accesso programmatico per rilevare il tipo di file Visio.
#### **Aggiunge il metodo DetectFileFormat nella classe FileFormatUtil**
Rileva e restituisce le informazioni sul formato di un Visio diagram memorizzato in un file.
#### **Aggiunge la proprietà FileFormatType nella classe FileFormatInfo**
Ottiene il formato di file rilevato.
#### **Aggiunge la proprietà LoadFormat in FileFormatInfo**
Ottiene il formato di caricamento rilevato.
#### **Aggiunge la proprietà ExportHiddenPage nelle classi SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions e PdfSaveOptions**
Definisce se è necessario esportare o meno le pagine Visio nascoste.
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

- [Controlla l'esportazione di pagine nascoste Visio al salvataggio](/diagram/it/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/#control-the-export-of-hidden-visio-pages-on-saving)
- [Rileva il formato del file Visio](/diagram/it/net/introduction/#detect-the-format-of-visio-file)
