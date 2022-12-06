---
title: Recupero delle informazioni sui caratteri
type: docs
weight: 80
url: /it/net/retrieving-font-information/
---
## **VSTO**
Di seguito è riportato il codice per il recupero delle informazioni sui caratteri:

{{< highlight "cs" >}}

  foreach (Font font in Application.ActiveDocument.Fonts)

 {

    //Display information about the fonts

    MessageBox.Show(font.Name);

 }

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram dispone di meccanismi per recuperare informazioni sugli elementi che compongono un diagram, da[pagine](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) , stampini,[connettori](/diagram/it/net/retrieving-connector-information/) anche i caratteri. Questo articolo mostra come scoprire quali caratteri sono utilizzati in un diagram.

{{% /alert %}} 

 Il[Font](https://reference.aspose.com/diagram/net/aspose.diagram/font) oggetto rappresenta un carattere tipografico applicato al testo in un documento o disponibile per l'uso nel sistema.

Un oggetto Font associa un nome (ad esempio, "Arial") all'ID del carattere (ad esempio, 3) che Microsoft Visio memorizza in una cella Font in una sezione Carattere di una forma che contiene testo formattato con tale carattere. Gli ID font possono cambiare quando un documento viene aperto su sistemi diversi o quando i font vengono installati o rimossi.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)

 {

    //Display information about the fonts

    Console.WriteLine(font.Name);

 }

{{< /highlight >}}
## **Scarica il codice di esempio**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Scarica il codice in esecuzione**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Font%20Information)
