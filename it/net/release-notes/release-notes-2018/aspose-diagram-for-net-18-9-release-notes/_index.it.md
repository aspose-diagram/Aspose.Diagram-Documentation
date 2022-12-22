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
|DIAGRAMNET-51509|VSDX to PNG - Line opacity lost in output image|Aumento|
|DIAGRAMNET-51510|VSDX to SVG - Line opacity lost in output image|Aumento|
|DIAGRAMNET-51516|Unisci più file VISIO in un unico output|Aumento|
|DIAGRAMNET-50272|VSD to SVG conversion - Some connection points have wrong position and size|Insetto|
|DIAGRAMNET-50273|VSD to SVG - The alignment of shape text items are incorrect|Insetto|
|DIAGRAMNET-50487|VSD to HTML - Slash character between the value is misplaced|Insetto|
|DIAGRAMNET-50975|VSDX to PDF - Background color of the shape is black|Insetto|
|DIAGRAMNET-50976|VSDX to HTML - Background color of the shape is black|Insetto|
|DIAGRAMNET-50980|VSDX to PNG - Numbers inside the diamond shapes are misplaced|Insetto|
|DIAGRAMNET-51129|The text items are not aligned properly on converting a VSD to PDF|Insetto|
|DIAGRAMNET-51511|Additional arrowheads in PNG conversion|Insetto|
|DIAGRAMNET-51512|Additional arrowheads showing in SVG conversion|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
#### **Aggiunto il metodo Combina nella classe Diagram**
Combina un oggetto Diagram con un altro oggetto Diagram.

{{< highlight "java" >}}

             Diagram diagramF = new Diagram( "f.vsdx");

            Diagram diagramS = new Diagram( "s.vsdx");

            diagramF.Combine(diagramS);

{{< /highlight >}}
