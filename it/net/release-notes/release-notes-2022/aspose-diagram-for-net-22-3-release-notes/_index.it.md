---
title: Aspose.Diagram for .NET 22.3 Note di rilascio
type: docs
weight: 25
url: /it/net/aspose-diagram-for-net-22-3-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 22.3.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-52667|shape.RefreshShape() non funziona per riflettere il valore BeginY modificato|Aumento|
|DIAGRAMNET-52668|Geometry NoShow Formula Risultati non aggiornati|Aumento|
|DIAGRAMNET-52655|App: il caricamento di vsd della vecchia versione e il salvataggio in pdf genera un'eccezione|Insetto|
|DIAGRAMNET-52661|Nessun esempio di aggiunta di filigrana a visio è fornito nella documentazione|Insetto|
|DIAGRAMNET-52663|Rileva gli stili di linea personalizzati per la forma con master nullo|Insetto|
|DIAGRAMNET-52666|Conversione da Visio a Pdf - Problema con la grafica dei dati [Cont.]|Insetto|
|DIAGRAMNET-52684|Exception when export to HTML|Insetto|
|DIAGRAMNET-52685|Exception when export to HTML|Insetto|
|DIAGRAMNET-52692|Diagram.Save to MemoryStream using PDF Format Throws a System.NullReferenceException|Insetto|

## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.

### **Aggiunge AddText nella pagina**
- Aggiunge testo con PinX e PinY definiti.

{{< highlight "java" >}}
double pinx = page.PageSheet.PageProps.PageWidth.Value / 2;
double piny = page.PageSheet.PageProps.PageHeight.Value / 2;
double width = page.PageSheet.PageProps.PageWidth.Value;
double height = page.PageSheet.PageProps.PageHeight.Value;
Shape shape = page.AddText(pinx, piny, width, height, "Test text", "Calibri", "#a5a5a5", 0.25);
{{< /highlight >}}
