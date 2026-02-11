---
title: Crea il documento Visio a livello di codice
linktitle: Crea documento Visio
type: docs
weight: 10
url: /it/net/create-visio-document/
description: Questa pagina descrive come creare il documento Visio da zero con la libreria Aspose.Diagram.
---
## **Creazione di un nuovo disegno Visio**
Aspose.Diagram for .NET consente di leggere e creare Microsoft Visio diagrammi dall'interno delle proprie applicazioni, senza Microsoft Office Automazione. Il primo passaggio durante la creazione di nuovi documenti è creare un diagram. Quindi aggiungere forme e connettori per creare il diagram.
## **Crea Visio Esempio di programmazione del disegno**
Il codice seguente mostra come creare un nuovo disegno Microsoft Visio. Si prega di notare che il disegno vuoto contiene una singola pagina vuota.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Initialize a Diagram class
Diagram diagram = new Diagram();

// Save diagram in the VSDX format
diagram.Save(dataDir + "CreateNewVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

{{% alert color="primary" %}} 

Il formato della carta da disegno è Lettera per impostazione predefinita.

{{% /alert %}} 

