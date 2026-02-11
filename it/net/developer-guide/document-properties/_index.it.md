---
title: Gestisci le proprietà del documento
linktitle: Proprietà del documento
type: docs
weight: 80
url: /it/net/document-properties/
description: Gestisci le proprietà del documento dei file visio.
---
## **introduzione**

Microsoft Visio offre la possibilità di aggiungere proprietà ai file visio. Queste proprietà del documento forniscono informazioni utili e sono suddivise in 2 categorie come descritto di seguito.

- Proprietà (integrate) definite dal sistema: le proprietà integrate contengono informazioni generali sul documento come titolo del documento, nome dell'autore, statistiche del documento e così via.
- Proprietà (personalizzate) definite dall'utente: proprietà personalizzate definite dall'utente finale sotto forma di coppia nome-valore.

{{% alert color="primary" %}}

Il punto più importante da sapere sulle proprietà predefinite e personalizzate è che è possibile accedere e modificare le proprietà predefinite, ma non crearle o rimuoverle. Tuttavia, è possibile creare e gestire proprietà personalizzate.

{{% /alert %}}

## **Gestione delle proprietà del documento utilizzando Microsoft Visio**

 Microsoft Visio consente di gestire le proprietà del documento dei file Visio in modalità WYSIWYG. Si prega di seguire i passaggi seguenti per aprire il file**Proprietà** dialogo in Visio 2016.

1.  Dal**File** menù, selezionare**Informazioni**.

|**Selezionando Menu Informazioni**|
|:- |
|![cose da fare:immagine_alt_testo](managing-document-properties_1.png)|
1.  Clicca su**Proprietà** voce e selezionare "Proprietà avanzate".

|**Facendo clic su Selezione proprietà avanzate**|
|:- |
|![cose da fare:immagine_alt_testo](managing-document-properties_2.png)|
1. Gestisci le proprietà del documento del file.

|**Finestra di dialogo Proprietà**|
|:- |
|![cose da fare:immagine_alt_testo](managing-document-properties_3.png)|
Nella finestra di dialogo Proprietà, ci sono diverse schede, come Generale, Riepilogo, Statistiche, Contenuti e Personalizzazioni. Ogni scheda consente di configurare diversi tipi di informazioni relative al file. La scheda Personalizzato viene utilizzata per gestire le proprietà personalizzate.

## **Lavorare con le proprietà del documento usando Aspose.Diagram**

Gli sviluppatori possono gestire dinamicamente le proprietà del documento utilizzando le API Aspose.Diagram. Questa funzione aiuta gli sviluppatori a memorizzare informazioni utili insieme al file, ad esempio quando il file è stato ricevuto, elaborato, timestamp e così via.

{{% alert color="primary" %}}

Aspose.Diagram for .NET scrive direttamente le informazioni su API e il numero di versione nei documenti di output.

Si prega di notare che non è possibile incaricare Aspose.Diagram for .NET di modificare o rimuovere queste informazioni dai documenti di output.

{{% /alert %}}

### **Accesso alle proprietà del documento**

 Aspose.Diagram Le API supportano entrambi i tipi di proprietà del documento, integrate e personalizzate. Aspose.Diagram'[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram) class rappresenta un file Visio e, come un file visio, il[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram) la classe può contenere più pagine, ognuna rappresentata da[**Pagina**](https://reference.aspose.com/diagram/net/aspose.diagram/page) class mentre la raccolta di pagine è rappresentata dal[**Collezione di pagine**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection)classe.

 Utilizzare il[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram)per accedere alle proprietà del documento del file come descritto di seguito.

- Per accedere alle proprietà predefinite del documento, utilizzare[**diagram.DocumentProps**](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties).
-  Per accedere alle proprietà del documento personalizzate, utilizzare[**diagram.DocumentProps.CustomProps**](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties/properties/customprops).

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//// Display Visio version and document modification time at different stages 
Console.WriteLine("Visio Instance Version : " + diagram.Version);
Console.WriteLine("Full Build Number Created : " + diagram.DocumentProps.BuildNumberCreated);
Console.WriteLine("Full Build Number Edited : " + diagram.DocumentProps.BuildNumberEdited);
Console.WriteLine("Date Created : " + diagram.DocumentProps.TimeCreated);
Console.WriteLine("Date Last Edited : " + diagram.DocumentProps.TimeEdited);
Console.WriteLine("Date Last Printed : " + diagram.DocumentProps.TimePrinted);
Console.WriteLine("Date Last Saved : " + diagram.DocumentProps.TimeSaved);
Console.WriteLine("CustomProps Length " + diagram.DocumentProps.CustomProps.Count);

{{< /highlight >}}
```

### **Aggiunta o rimozione di proprietà del documento personalizzate**

Come descritto in precedenza all'inizio di questo argomento, gli sviluppatori non possono aggiungere o rimuovere proprietà predefinite perché queste proprietà sono definite dal sistema, ma è possibile aggiungere o rimuovere proprietà personalizzate perché sono definite dall'utente.

### **Aggiunta di proprietà personalizzate**

 Aspose.Diagram API hanno esposto il file[**Aggiungere**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection/methods/add) metodo per il[**Collezione CustomProp**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection)class per aggiungere proprietà personalizzate alla raccolta.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//// Get CustomProperties of diagram
Aspose.Diagram.CustomPropCollection customProperties = diagram.DocumentProps.CustomProps;
//Set property of CustomProp
Aspose.Diagram.CustomProp customProp = new Aspose.Diagram.CustomProp();
customProp.PropType = Aspose.Diagram.PropType.String;
customProp.CustomValue.ValueString = "Test";
//Add CustomProp to Collection
customProperties.Add(customProp);

{{< /highlight >}}
```

### **Rimozione delle proprietà personalizzate**

 Per rimuovere le proprietà personalizzate utilizzando Aspose.Diagram, chiama il[**CustomPropCollection.Remove**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection/methods/remove)metodo e passare il nome della proprietà del documento da rimuovere.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RemovingCustomProperties.cs" >}}
