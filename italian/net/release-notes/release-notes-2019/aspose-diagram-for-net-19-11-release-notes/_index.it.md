---
title: Aspose.Diagram for .NET Note sulla versione 19.11
type: docs
weight: 20
url: /it/net/aspose-diagram-for-net-19-11-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene informazioni sulle note di rilascio per Aspose.Diagram for .NET 19.11.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riepilogo**|**Categoria**|
|:- |:- |:- |
|DIAGRAMNET-50004| Aggiungi supporto a[applicare il foglio di stile](/diagram/it/net/format-visio-pages/) per pagina intera|Aumento|
|DIAGRAMNET-50576|Aggiunto il supporto per eliminare un oggetto di classe Diagram|Aumento|
|DIAGRAMNET-50098|Imposta il colore di sfondo della pagina|Insetto|
|DIAGRAMNET-51722|Diagram in SVG - l'immagine di output presenta errori|Insetto|
|DIAGRAMNET-51724|Errori nella console di Chrome durante la visualizzazione dell'output SVG|Insetto|
|DIAGRAMNET-51725|Recupera l'indice z delle forme in Diagram|Insetto|
|DIAGRAMNET-51726|Immagine di sfondo mancante (PowerPoint viene aggiunto in VISIO) durante la rimozione di forme e stili principali inutilizzati|Insetto|
|DIAGRAMNET-51727|CheckBox (controllo CheckBox) Mancante durante la rimozione di forme e stili principali inutilizzati|Insetto|
|DIAGRAMNET-51728|Linea mancante durante la rimozione di forme e stili principali inutilizzati|Insetto|

## **Pubblico API e modifiche incompatibili con le versioni precedenti**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata a Aspose.Diagram for .NET. In caso di dubbi su qualsiasi modifica elencata, si prega di segnalarlo su il forum di supporto Aspose.Diagram.
### **Aggiunto Applica stile nella pagina**
Applica lo stile a tutta pagina.

{{< highlight "java" >}}

StyleSheet st = new StyleSheet();

st.ID = dia.StyleSheets.Count + 1;

Aspose.Diagram.Char ch = new Aspose.Diagram.Char();

ch.Color.Value = "#00ff00";

ch.IX = 0;

st.Chars.Add(ch);

st.Line.LineColor.Value = "#ff0000";

st.Line.LinePattern.Value = 1;

st.Line.LineWeight.Value = 0.01;

st.Fill.FillForegnd.Value = "#0000ff";

st.Fill.FillPattern.Value = 1;

st.Fill.ShdwPattern.Value = 0;

dia.StyleSheets.Add(st);

foreach (Shape shape in dia.Pages[0].Shapes)

{

     shape.Line.LinePattern.Value = 1;
    
     shape.Fill.FillPattern.Value = 1;

}

dia.Pages[0].ApplyStyle(st.ID, st.ID, st.ID);

{{< /highlight >}}
### **Aggiunto Smaltire in Diagram**
Esegue attività definite dall'applicazione associate alla liberazione, al rilascio o al ripristino delle risorse non gestite.

{{< highlight "java" >}}

 diagram.Dispose();

{{< /highlight >}}
