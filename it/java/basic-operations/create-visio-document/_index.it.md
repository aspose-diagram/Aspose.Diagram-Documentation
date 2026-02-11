---
title: Crea il documento Visio a livello di codice
linktitle: Crea documento Visio
type: docs
weight: 10
url: /it/java/create-visio-document/
description: Questa pagina descrive come creare il documento Visio da zero con la libreria Aspose.Diagram.
---
## **Creazione di un nuovo disegno Visio**
Aspose.Diagram for Java consente di leggere e creare Microsoft Visio diagrammi dall'interno delle proprie applicazioni, senza Microsoft Office Automazione. Il primo passaggio durante la creazione di nuovi documenti è creare un diagram. Quindi aggiungere forme e connettori per creare il diagram.
### **Crea Visio Esempio di programmazione del disegno**
Il codice seguente mostra come creare un nuovo disegno Microsoft Visio. Si prega di notare che il disegno vuoto contiene una singola pagina vuota.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}} 

Il formato della carta da disegno è Lettera per impostazione predefinita.

{{% /alert %}} 

