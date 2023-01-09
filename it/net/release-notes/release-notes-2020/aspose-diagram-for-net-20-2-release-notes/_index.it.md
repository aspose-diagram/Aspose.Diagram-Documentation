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
|DIAGRAMNET-51748|Add PNG to Diagram - transparency is lost|Insetto|
|DIAGRAMNET-51749|Si verifica un errore durante il salvataggio del documento Visio|Insetto|
|DIAGRAMNET-51751|VSDX to PNG - Extra image is shown|Insetto|
|DIAGRAMNET-51752|VSDX to PNG - Extra space is shown|Insetto|
|DIAGRAMNET-51753|VSDX to PNG - Icons position is changing|Insetto|
|DIAGRAMNET-51754|VSDX to PNG - Question mark icon position is changed|Insetto|
|DIAGRAMNET-51762|PDF generated is different comparing to the input Visio diagram|Insetto|
|DIAGRAMNET-51763|VSDX to PNG - Information is missing in the output|Insetto|
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




