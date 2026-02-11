---
title: Inserisci un controllo ActiveX nel Visio Diagram
type: docs
weight: 10
url: /it/net/insert-an-activex-control-in-the-visio-diagram/
description: Questa pagina descrive come inserire un controllo activeX con la libreria Aspose.Diagram.
---
{{% alert color="primary" %}}

 Gli sviluppatori possono aggiungere controlli ActiveX direttamente ai disegni Microsoft Visio per rendere interattivi i disegni Visio diagram utilizzando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Inserire un esempio di programmazione di controlli ActiveX**
[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class offre il metodo AddActiveXControl e consente agli sviluppatori di inserire qualsiasi tipo di controllo ActiveX come pulsante di comando, casella combinata, casella di controllo, casella di riepilogo, casella di testo, pulsante di selezione, pulsante di opzione, etichetta, immagine, pulsante di commutazione e barra di scorrimento.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioActiveXControls();
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);
// Save diagram
diagram.Save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
