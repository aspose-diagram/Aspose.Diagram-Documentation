---
title: Aspose.Diagram for .NET 20.2 Note di rilascio
type: docs
weight: 60
url: /it/net/aspose-diagram-for-net-20-2-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 20.2.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51747|Modifiche ai file dopo la conversione Visio vsd->vsdx|Aumento|
|DIAGRAMNET-51750|Aggiunta flag "HasHiddenInfo"|Aumento|
|DIAGRAMNET-51748|Aggiungi PNG a Diagram - la trasparenza è persa|Insetto|
|DIAGRAMNET-51749|Si verifica un errore durante il salvataggio del documento Visio|Insetto|
|DIAGRAMNET-51751|VSDX in PNG: viene mostrata un'immagine aggiuntiva|Insetto|
|DIAGRAMNET-51752|VSDX in PNG: viene visualizzato spazio extra|Insetto|
|DIAGRAMNET-51753|VSDX in PNG - La posizione delle icone sta cambiando|Insetto|
|DIAGRAMNET-51754|VSDX in PNG - La posizione dell'icona del punto interrogativo è stata modificata|Insetto|
|DIAGRAMNET-51762|Il PDF generato è diverso rispetto all'input Visio diagram|Insetto|
|DIAGRAMNET-51763|VSDX in PNG: mancano informazioni nell'output|Insetto|
## ` `**Public API e modifiche incompatibili con le versioni precedenti**
` `Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. il forum di supporto Aspose.Diagram.
### **Aggiunto EnlargePage in ImageSaveOptions**
- Specifica se ingrandire la pagina

{{< highlight "java" >}}

 Aspose.Diagram.Saving.ImageSaveOptions opt = new Aspose.Diagram.Saving.ImageSaveOptions(Aspose.Diagram.SaveFileFormat.PNG);

opt.EnlargePage = false;

{{< /highlight >}}
### **Aggiunto HasHiddenInfo in Diagram**
- Indica se questo diagram ha informazioni nascoste.



{{< highlight "java" >}}

 diagram.HasHiddenInfo();

{{< /highlight >}}




