---
title: Raggruppa, converti e verifica le forme
type: docs
weight: 80
url: /it/net/group-convert-and-verify-shapes/
description: Questa sezione spiega come raggruppare le forme con Aspose.Diagram.
---
## **Raggruppa più forme insieme nel disegno Visio**
Aspose.Diagram API consente agli sviluppatori di raggruppare le forme insieme per spostarle tutte in una volta. Ogni forma in un gruppo mantiene un'identità univoca e ha il proprio insieme di proprietà. Quando cambiamo la formattazione di un gruppo di forme, assegna la nuova proprietà a ciascuna forma.
### **Come raggruppare le forme**
 Il metodo di gruppo esposto dal[Collezione Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class può essere utilizzato per raggruppare le forme insieme.

Il codice seguente mostra come:

1. Carica un campione diagram.
1. inizializzato un array delle forme
1. ottenere una forma particolare per id.
1. ottieni un'altra particolare forma particolare per id.
1. assegnare forme all'array.
1. raggruppare le forme chiamando il metodo Group.
1. salvo diagram
#### **Esempio di programmazione delle forme di gruppo**
Utilizzare il seguente codice nell'applicazione .NET per raggruppare le forme utilizzando Aspose.Diagram for .NET API.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GroupShapes-GroupShapes.cs" >}}
## **Converti una forma Visio in altri formati di file**
Aspose.Diagram for .NET API consente agli sviluppatori di convertire una singola forma Visio in qualsiasi altro formato di file supportato. In questo articolo rimuoviamo tutte le altre forme Visio dalla pagina e personalizziamo le impostazioni della pagina in base alla dimensione della forma di origine.
### **Conversione di una particolare forma Visio**
 Gli sviluppatori possono convertire una forma Visio in PDF, HTML, immagine, SVG e SWF tramite**specificando le opzioni di salvataggio Visio**.
Questo codice di esempio funziona come segue:

1. Carica una fonte Visio.
1. Ottieni una pagina particolare.
1. Rimuovi la pagina di sfondo.
1. Costruisci una tabella hash di tutte le forme che contengono gli ID e i nomi.
1. Itera attraverso la tabella hash
1. Rimuovi tutte le forme dalla pagina Visio, tranne quella in particolare.
1. Imposta la dimensione della pagina.
1. Salva la pagina Visio in qualsiasi formato di file supportato.
#### **Esempio di programmazione di forme convertite**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.cs" >}}
### **Converti Visio Shape in PDF**
Il metodo ToPdf della classe Shape permette di convertire una forma nel formato PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Converti la forma Visio in HTML**
Il metodo ToHTML della classe Shape permette di convertire una forma nel formato HTML.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
## **Verifica se due forme Visio sono collegate o incollate**
 Aspose.Diagram for .NET API consente agli sviluppatori di verificare che le due forme Visio siano incollate o collegate. In precedenza, abbiamo visto come collegare o incollare due forme in questi argomenti della guida:[Aggiungi e collega Visio Forme](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) e[Forme di colla all'interno del contenitore](/diagram/it/net/working-with-shapes-gluing/).
### **Verifica delle Forme Connesse o Incollate**
 Il[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) offre le proprietà IsGlued e IsConnected per determinare se due forme sono collegate o connesse.
#### **Esempio di programmazione per la verifica di forme connesse o incollate**
La parte di codice seguente verifica se due forme sono connesse o incollate.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.cs" >}}
## **Verificare se la forma Visio si trova in un gruppo di forme**
Aspose.Diagram for .NET API consente agli sviluppatori di verificare se la forma Visio si trova o meno in un gruppo di forme.
### **Verifica della forma nel gruppo delle forme**
Il[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)offre proprietà IsInGroup per determinare se la forma Visio è in una forma di gruppo.
#### **Verifica della forma nell'esempio di programmazione del gruppo di forme**
La parte di codice seguente verifica se la forma è in una forma di gruppo.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.cs" >}}
