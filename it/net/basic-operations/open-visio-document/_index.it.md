---
title: Apri il documento Visio a livello di codice
linktitle: Apri il documento Visio
type: docs
weight: 20
url: /it/net/open-visio-document/
description: Questa pagina descrive come aprire il documento Visio da zero con la libreria Aspose.Diagram.
---
## **Leggi un disegno esistente Visio**
Aspose.Diagram API supporta la creazione da zero dei nuovi diagrammi Visio e quindi il salvataggio in qualsiasi formato di file supportato. Gli sviluppatori possono anche caricare un Visio diagram esistente per scopi di modifica, aggiunta o elaborazione.
## **Leggendo un Diagram**
Utilizzando Aspose.Diagram API, gli sviluppatori possono caricare tutti i formati di file Visio supportati. I costruttori disponibili della classe Diagram lo consentono e accettano una stringa di percorso file valida o un flusso di file del file sorgente Visio.

I formati di file leggibili supportati sono i seguenti:
**VSDX, VSD, VSDM, VSS, VSSX, VSSM, VTX, VSTM, VDX, VDW, VST, VSTX and VSX**

I costruttori della classe diagram offrono anche un parametro facoltativo che definisce LoadFileFormat o LoadOptions. Sono le informazioni di pre-caricamento che gli sviluppatori possono passare allo Aspose.Diagram API. Si consiglia di trasmettere le informazioni realistiche per ottenere prestazioni ideali.
## **Lettura Diagram Esempio di programmazione**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD stream
FileStream st = new FileStream(dataDir + "Drawing1.vsdx", FileMode.Open);
Diagram vsdDiagram = new Diagram(st);
st.Close();

// Call the diagram constructor to load a VDX diagram
Diagram vdxDiagram = new Diagram(dataDir + "Drawing1.vdx");

/*
 * Call diagram constructor to load a VSS stencil
 * providing load file format
*/
Diagram vssDiagram = new Diagram(dataDir + "Basic.vss", LoadFileFormat.VSS);

/*
 * Call diagram constructor to load diagram from a VSX file
 * providing load options
*/
LoadOptions loadOptions = new LoadOptions(LoadFileFormat.VSX);
Diagram vsxDiagram = new Diagram(dataDir + "Drawing1.vsx", loadOptions);

{{< /highlight >}}

