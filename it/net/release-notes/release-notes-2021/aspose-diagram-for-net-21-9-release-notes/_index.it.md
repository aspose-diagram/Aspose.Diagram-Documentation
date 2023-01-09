---
title: Aspose.Diagram for .NET 21.9 Note di rilascio
type: docs
weight: 4
url: /it/net/aspose-diagram-for-net-21-9-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 21.9.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-50164|La revisione del layout dell'opzione CompactTree non funziona come previsto|Aumento|
|DIAGRAMNET-50997|Impossibile impostare le opzioni di layout di un VDX diagram|Aumento|
|DIAGRAMNET-52117|Aggiungi il supporto del token di annullamento sul metodo Diagram|Aumento|
|DIAGRAMNET-52196|Caricamento e salvataggio del testo del campo perso vsdx|Aumento|
|DIAGRAMNET-52197|Il caricamento e il salvataggio di vsdx cambiano il valore di DisplayMode|Aumento|
|DIAGRAMNET-52205|Evento doppio clic mancante dalla forma|Aumento|
|DIAGRAMNET-51877|Eccezione "Parametro non valido" durante il rendering del file VSD|Insetto|
|DIAGRAMNET-52114|"Parameter is not valid." exception when rendering VSD file to PNG/JPG|Insetto|
|DIAGRAMNET-52124|Salvare Visio come problema html|Insetto|
|DIAGRAMNET-52127|Saving Visio with helper lines to HTML issue|Insetto|
|DIAGRAMNET-52148|VSDX to PDF - Strikethrough text is not correct in PDF|Insetto|
|DIAGRAMNET-52150|Impossibile estrarre il valore della formula di cella definita dall'utente CONT.|Insetto|
|DIAGRAMNET-52229|La cella definita dall'utente viene rinominata|Insetto|
|DIAGRAMNET-52231|L'opzione "colla" del connettore per modellare è persa|Insetto|
|DIAGRAMNET-52252|Il contorno della forma viene tagliato durante il salvataggio di visio in html|Insetto|
|DIAGRAMNET-52253|Dopo aver salvato il file .vtx in .vsdx, il connettore aggiunto dallo stencil è rotto|Insetto|
|DIAGRAMNET-52266|Impossibile rimuovere le celle definite dall'utente|Insetto|

## **Public API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.

### **Aggiunge DependsOnShapes in Shape**
- Restituisce una matrice che contiene gli identificatori delle forme che dipendono da una forma.



{{< highlight "java" >}}

long[]shapeids = shape.DependsOnShapes();

{{< /highlight >}}



