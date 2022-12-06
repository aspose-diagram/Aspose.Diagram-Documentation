---
title: Aspose.Diagram for .NET 18.9 Note di rilascio
type: docs
weight: 40
url: /it/net/aspose-diagram-for-net-18-9-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 18.9](https://www.nuget.org/packages/Aspose.Diagram/18.9.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51509|Da VSDX a PNG: opacità della linea persa nell'immagine di output|Aumento|
|DIAGRAMNET-51510|VSDX in SVG - Opacità della linea persa nell'immagine di output|Aumento|
|DIAGRAMNET-51516|Unisci più file VISIO in un unico output|Aumento|
|DIAGRAMNET-50272|Conversione da VSD a SVG - Alcuni punti di connessione hanno posizione e dimensioni errate|Insetto|
|DIAGRAMNET-50273|VSD in SVG - L'allineamento degli elementi di testo della forma non è corretto|Insetto|
|DIAGRAMNET-50487|VSD in HTML - Il carattere barra tra il valore è fuori posto|Insetto|
|DIAGRAMNET-50975|VSDX in PDF - Il colore di sfondo della forma è nero|Insetto|
|DIAGRAMNET-50976|VSDX in HTML: il colore di sfondo della forma è nero|Insetto|
|DIAGRAMNET-50980|VSDX in PNG - I numeri all'interno delle forme del diamante sono fuori posto|Insetto|
|DIAGRAMNET-51129|Gli elementi di testo non sono allineati correttamente durante la conversione di un VSD in PDF|Insetto|
|DIAGRAMNET-51511|Punte di freccia aggiuntive nella conversione PNG|Insetto|
|DIAGRAMNET-51512|Frecce aggiuntive mostrate nella conversione SVG|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
#### **Aggiunto il metodo Combina nella classe Diagram**
Combina un oggetto Diagram con un altro oggetto Diagram.

{{< highlight "java" >}}

             Diagram diagramF = new Diagram( "f.vsdx");

            Diagram diagramS = new Diagram( "s.vsdx");

            diagramF.Combine(diagramS);

{{< /highlight >}}
