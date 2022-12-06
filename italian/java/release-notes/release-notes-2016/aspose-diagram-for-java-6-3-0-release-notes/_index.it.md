---
title: Aspose.Diagram for Java 6.3.0 Note di rilascio
type: docs
weight: 90
url: /it/java/aspose-diagram-for-java-6-3-0-release-notes/
---
## **Altri miglioramenti e modifiche**

|**Chiave** |**Riepilogo** |**Categoria** |
|:- |:- |:- |
| DIAGRAMMAJava-50306| Aggiungere il supporto per il rilevamento del tipo Visio diagram.| Nuova caratteristica|
| DIAGRAMMAJava-50311| Impedisci l'esportazione delle pagine Visio nascoste nel PDF.| Nuova caratteristica|
| DIAGRAMMAJava-50312| Impedisci l'esportazione delle pagine Visio nascoste nell'HTML.| Nuova caratteristica|
| DIAGRAMMAJava-50313| Impedisci l'esportazione delle pagine Visio nascoste nel PNG.| Nuova caratteristica|
| DIAGRAMMAJava-50314| Impedisci l'esportazione delle pagine Visio nascoste nel JPEG.| Nuova caratteristica|
|DIAGRAMMAJava-50315| Impedisci l'esportazione delle pagine Visio nascoste nell'SVG.| Nuova caratteristica|
| DIAGRAMMAJava-50316| Impedisci l'esportazione delle pagine Visio nascoste nella GIF.| Nuova caratteristica|
| DIAGRAMMAJava-50317| Impedisci l'esportazione delle pagine Visio nascoste nell'XPS.| Nuova caratteristica|
| DIAGRAMMAJava-50307| L'esportazione da VDX a VSDX contrassegna l'opzione della linea della griglia della pagina selezionata.| Insetto|
| DIAGRAMMAJava-50308| La routine di apertura e salvataggio di VSDX trasforma il testo in caratteri fittizi.| Insetto|
| DIAGRAMMAJava-50309| La routine di apertura e salvataggio di VSDX ha modificato la forma della linea tratteggiata.| Insetto|
| DIAGRAMMAJava-50310| La routine di apertura e salvataggio di VSDX modifica il carattere e l'audacia del testo.| Insetto|
| DIAGRAMMAJava-50318| L'esportazione da VSD a VDX genera l'errore dell'elemento principale.| Insetto|
### **Pubblico API e modifiche incompatibili con le versioni precedenti**
Consulta l'elenco per eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for Java. Se hai dubbi su qualsiasi modifica elencata, segnalala sul[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
#### **Aggiungere le classi FileFormatUtil e FileFormatInfo.**
Queste classi forniscono l'accesso programmatico per rilevare il tipo di file Visio.
#### **Aggiunge il metodo detectFileFormat nella classe FileFormatUtil.**
Rileva e restituisce le informazioni sul formato di un Visio diagram memorizzato in un file.
#### **Aggiunge la proprietà FileFormatType nella classe FileFormatInfo**
Ottiene il formato di file rilevato.
#### **Aggiunge la proprietà LoadFormat in FileFormatInfo**
Ottiene il formato di caricamento rilevato.
#### **Aggiunge setExportHiddenPage in SVGSaveOptions, XPSSaveOptions,ImageSaveOptions,HTMLSaveOptions,PdfSaveOptions**
Definisce se è necessario esportare o meno le pagine Visio nascoste.
### **Esempi di utilizzo**
Si prega di controllare l'elenco degli argomenti della guida aggiunti nei documenti Wiki Aspose.Diagram:

- [Controlla l'esportazione di pagine nascoste Visio al salvataggio]()
- [Rileva il formato del file Visio]()
