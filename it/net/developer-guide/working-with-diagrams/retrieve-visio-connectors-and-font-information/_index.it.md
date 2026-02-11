---
title: Recupera i connettori Visio e le informazioni sui caratteri
type: docs
weight: 20
url: /it/net/retrieve-visio-connectors-and-font-information/
description: Questa sezione spiega come ottenere i connettori visio e le informazioni sui font.
---
## **Recupero delle informazioni sul connettore**
 Aspose.Diagram for .NET fornisce meccanismi per il recupero di informazioni - ID e nome - su[pagine](/diagram/it/net/retrieve-2c-get-2c-copy-and-insert-a-page/) e[maestro](https://docs.aspose.com/diagram/net/working-with-masters/). Consente inoltre di ottenere informazioni sui connettori, gli elementi che collegano le forme.

 Il[Collegare](http://www.aspose.com/api/net/diagram/aspose.diagram/connect) oggetto rappresenta un connettore che unisce due forme in una pagina di disegno Visio. La proprietà Connects, esposta da[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class supporta una raccolta di oggetti Aspose.Diagram.Connect. Questa proprietà può essere utilizzata per recuperare informazioni su ID e nome su un connettore.
### **Esempio di programmazione**
La parte di codice seguente recupera le informazioni per i connettori in un diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveConnectorInfo.vsd");

foreach (Aspose.Diagram.Connect connector in vdxDiagram.Pages[0].Connects)
{
    // Display information about the Connectors
    Console.WriteLine("\nFrom Shape ID : " + connector.FromSheet);
    Console.WriteLine("To Shape ID : " + connector.ToSheet);
}

{{< /highlight >}}
```
## **Recupero delle informazioni sui caratteri**
 Aspose.Diagram dispone di meccanismi per recuperare informazioni sugli elementi che compongono un diagram, da[pagine](/diagram/it/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [stencil](https://docs.aspose.com/diagram/net/working-with-masters/), [connettori](/diagram/it/net/retrieving-connector-information/) anche i caratteri. Questo articolo mostra come scoprire quali caratteri sono utilizzati in un diagram.

 Il[Font](http://www.aspose.com/api/net/diagram/aspose.diagram/font) oggetto rappresenta un carattere tipografico applicato al testo in un documento o disponibile per l'uso nel sistema. Un oggetto Font associa un nome (ad esempio, "Arial") all'ID del carattere (ad esempio, 3) che Microsoft Visio memorizza in una cella Font in una sezione Carattere di una forma che contiene testo formattato con tale carattere. Gli ID font possono cambiare quando un documento viene aperto su sistemi diversi o quando i font vengono installati o rimossi.
### **Recupero dell'esempio di programmazione dei caratteri**
Il seguente pezzo di codice recupera le informazioni sui font dal Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");

foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)
{
    // Display information about the fonts
    Console.WriteLine(font.Name);
}

{{< /highlight >}}
```
### **Ottenere la directory dei caratteri predefinita**
Aspose.Diagram for .NET API consente inoltre di ottenere il percorso predefinito della directory dei caratteri utilizzando il metodo GetDefaultFontDir() della classe Diagram. La parte di codice seguente recupera la directory dei font predefinita da Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");
           
// Display font default directory
Console.WriteLine(vdxDiagram.GetDefaultFontDir());

{{< /highlight >}}
```
### **Ottenere caratteri inutilizzati**
{{% alert color="primary" %}}

Questo metodo è supportato dalla versione 19.6 o successiva.

{{% /alert %}}

Aspose.Diagram for .NET API consente inoltre di ottenere font inutilizzati utilizzando il metodo GetUnusedStyles() della classe Diagram. Il seguente pezzo di codice recupera i caratteri inutilizzati dal Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "Sample_UnusedFonts.vsdx");

// Get Unused Fonts 
StyleSheetCollection unused = vdxDiagram.GetUnusedStyles();

// Display unused fonts count 
Console.WriteLine(unused.Count);

{{< /highlight >}}
```
