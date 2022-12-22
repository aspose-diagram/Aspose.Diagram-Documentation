---
title: Aspose.Diagram for .NET Note sulla versione 21.11
type: docs
weight: 2
url: /it/net/aspose-diagram-for-net-21-11-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 21.11.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-51111|Gradient fill of the circles is wrong when converting a VDX to EMF|Aumento|
|DIAGRAMNET-52377|Aggiunto il supporto per il caricamento di vsd con la vecchia versione 3|Aumento|
|DIAGRAMNET-51364|VSDX to PNG - missing the text of OLE Embedded object|Insetto|
|DIAGRAMNET-52329|VSDX to HTML - Emojis are not present in the output|Insetto|
|DIAGRAMNET-52345|I piè di pagina dell'intestazione vengono persi dopo aver salvato il file Diagram|Insetto|
|DIAGRAMNET-52349|Visio to HTML - Left and right edges are cut|Insetto|
|DIAGRAMNET-52374|ArgumentOutOfRangeException while saving to PDF|Insetto|
|DIAGRAMNET-52386|Perché alcune pagine diagram possono essere duplicate e altre non possono utilizzare Page.Copy()?|Insetto|

## **Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.


### **Aggiunge PresetTheme in Shape**
- Applica un tema preimpostato a questa forma.

{{< highlight "java" >}}

shape.PresetTheme = PresetThemeValue.Bubble;

{{< /highlight >}}


### **Aggiunge PresetThemeVariant in Shape**
- Applica una variante del tema preimpostato a questa forma

{{< highlight "java" >}}

shape.PresetThemeVariant = PresetThemeVariantValue.Variant1;

{{< /highlight >}}

### **Aggiunge PresetThemeQuickStyle in Shape**
- Applicare uno stile rapido della variante del tema preimpostato a questa forma

{{< highlight "java" >}}

 shape.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle1;

{{< /highlight >}}
