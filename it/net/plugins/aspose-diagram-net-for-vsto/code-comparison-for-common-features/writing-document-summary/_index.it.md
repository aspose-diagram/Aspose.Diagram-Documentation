---
title: Riassunto del documento di scrittura
type: docs
weight: 70
url: /it/net/writing-document-summary/
---
## **VSTO**
Di seguito il codice per scrivere il riepilogo del documento Visio:

{{< highlight "cs" >}}

  Application.ActiveDocument.Creator = "Zeeshan";

 Application.ActiveDocument.Company = "Aspose";

 Application.ActiveDocument.Category = "Drawing 2D";

 Application.ActiveDocument.Manager = "Self";

 Application.ActiveDocument.Title = "Zeeshan";

 Application.ActiveDocument.Subject = "Visio Diagram";


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Microsoft Visio consente di definire una serie di proprietà delle informazioni di riepilogo del documento per aiutare te e i tuoi colleghi a identificare un diagram. Le proprietà di riepilogo, ad esempio titolo, oggetto, autore e descrizione, rendono il file più facile da trovare durante la ricerca e più facile da riconoscere durante la navigazione File.

{{% /alert %}} 
### **Scrittura Microsoft Visio Documento Sintesi Info**
 Il[Proprietà documento](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties)class espone una serie di proprietà da impostare o ottenere informazioni di riepilogo Microsoft Visio diagram. Aspose.Diagram for .NET può aggiornare le informazioni di riepilogo del disegno e quindi riscrivere il file di disegno in VDX.

Per aggiornare le informazioni di riepilogo del disegno di un file VDX o VSD esistente:

1.  Crea un'istanza di[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) classe.
1. Impostare le proprietà esposte da Diagram.DocumentProps per definire le informazioni di riepilogo per il file di disegno Visio.
1. Chiamare il metodo Save della classe Diagram per scrivere il file di disegno Visio in VDX.

Controlla le informazioni di riepilogo:

1. Aprire il file di output VDX in Microsoft Visio.
1.  Selezione**Informazioni** dal**File** menù.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram("Drawing1.vdx");

 //Set some summary information about the diagram

 vdxDiagram.DocumentProps.Creator = "Ijaz";

 vdxDiagram.DocumentProps.Company = "Aspose";

 vdxDiagram.DocumentProps.Category = "Drawing 2D";

 vdxDiagram.DocumentProps.Manager = "Sergey Polshkov";

 vdxDiagram.DocumentProps.Title = "Aspose Title";

 vdxDiagram.DocumentProps.TimeCreated = DateTime.Now;

 vdxDiagram.DocumentProps.Subject = "Visio Diagram";

 vdxDiagram.DocumentProps.Template = "Aspose Template";

 //Write the updated file to the disk in VDX file format

 vdxDiagram.Save("output.vdx", SaveFileFormat.VDX);


{{< /highlight >}}
## **Scarica il codice di esempio**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Scarica il codice in esecuzione**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Writing%20Document%20Summary)
