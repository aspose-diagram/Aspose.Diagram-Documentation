﻿---
title: Aspose.Diagram for .NET 18.8 Note di rilascio
type: docs
weight: 50
url: /it/net/aspose-diagram-for-net-18-8-release-notes/
---
{{% alert color="primary" %}} 

 Questa pagina contiene le note di rilascio per[Aspose.Diagram for .NET 18.8](https://www.nuget.org/packages/Aspose.Diagram/18.8.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51500|Problema di rendering dell'immagine|Aumento|
|DIAGRAMNET-51504|Aggiungi il supporto per creare un nuovo revisore|Aumento|
|DIAGRAMNET-50953|The text items are displaced on converting a VSDX to PNG|Insetto|
|DIAGRAMNET-51122|The incorrect position of text items on converting a VSD to PDF|Insetto|
|DIAGRAMNET-51123|The text of the shapes is displaced on converting a VSD to PDF|Insetto|
|DIAGRAMNET-51408|VSD a Immagine - i caratteri si sovrappongono alla linea|Insetto|
|DIAGRAMNET-51499|Il metodo Diagram.Save genera OutOfMemoryException|Insetto|
|DIAGRAMNET-51501|Le forme si sovrappongono nel file VDX|Insetto|
|DIAGRAMNET-51505|Dots missing in generated PDF|Insetto|
## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di tutte le modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarli in il[Aspose.Diagram forum di supporto](https://forum.aspose.com/c/diagram/17).
#### **Aggiunge Revisore**
{{< highlight "java" >}}

             Reviewer viewer = new Reviewer();

            viewer.Name.Value = "test";

            viewer.ReviewerID.Value = 3;

{{< /highlight >}}



