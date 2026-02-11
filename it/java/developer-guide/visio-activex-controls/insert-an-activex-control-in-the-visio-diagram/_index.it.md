---
title: Inserisci un controllo ActiveX nel Visio Diagram
type: docs
weight: 10
url: /it/java/insert-an-activex-control-in-the-visio-diagram/
---
{{% alert color="primary" %}}

 Gli sviluppatori possono aggiungere controlli ActiveX direttamente ai disegni Microsoft Visio per rendere interattivi i disegni Visio diagram utilizzando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **Inserire un esempio di programmazione di controlli ActiveX**
[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class offre il metodo addActiveXControl e consente agli sviluppatori di inserire qualsiasi tipo di controllo ActiveX come pulsante di comando, casella combinata, casella di controllo, casella di riepilogo, casella di testo, pulsante di selezione, pulsante di opzione, etichetta, immagine, pulsante di commutazione e barra di scorrimento.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(InsertanActiveControl.class) + "VisioActiveXControls/";
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);
// Save diagram
diagram.save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
