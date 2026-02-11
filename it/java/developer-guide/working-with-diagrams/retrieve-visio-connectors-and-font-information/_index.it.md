---
title: Recupera i connettori Visio e le informazioni sui caratteri
type: docs
weight: 20
url: /it/java/retrieve-visio-connectors-and-font-information/
---
## **Recupero delle informazioni sul connettore**
 Aspose.Diagram for Java fornisce meccanismi per il recupero di informazioni - ID e nome - su[pagine](/diagram/it/java/retrieve-get-copy-and-insert-a-page/) e[maestro](). Consente inoltre di ottenere informazioni sui connettori, gli elementi che collegano le forme.

 Il[Collegare](https://reference.aspose.com/diagram/java/com.aspose.diagram/connect) oggetto rappresenta un connettore che unisce due forme in una pagina di disegno Visio. La proprietà Connects, esposta da[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class supporta una raccolta di oggetti Aspose.Diagram.Connect. Questa proprietà può essere utilizzata per recuperare informazioni su ID e nome su un connettore.

**Una finestra della console che mostra l'output del codice seguente.** 

![cose da fare:immagine_alt_testo](retrieve-visio-connectors-and-font-information_1.png)
### **Esempio di programmazione**
La parte di codice seguente recupera le informazioni per i connettori in un diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveConnectorInfo.class);
        
//Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "RetrieveConnectorInfo.vsd");        
for(Connect connector : (Iterable<Connect>) diagram.getPages().getPage(0).getConnects())
{
    // Display information about the Connectors
    System.out.println("\nFrom Shape ID : " + connector.getFromSheet());
    System.out.println("To Shape ID : " + connector.getToSheet());
 }

System.out.println("Process Completed Successfully");

{{< /highlight >}}

## **Recupero delle informazioni sui caratteri**
 Aspose.Diagram dispone di meccanismi per recuperare informazioni sugli elementi che compongono un diagram, da[pagine](/diagram/it/java/retrieve-get-copy-and-insert-a-page/), [stencil](), [connettori](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection) anche i caratteri. Questo articolo mostra come scoprire quali caratteri sono utilizzati in un diagram.

 Il[Font](https://reference.aspose.com/diagram/java/com.aspose.diagram/font) oggetto rappresenta un carattere tipografico applicato al testo in un documento o disponibile per l'uso nel sistema.

Un oggetto Font associa un nome (ad esempio, "Arial") all'ID del carattere (ad esempio, 3) che Microsoft Visio memorizza in una cella Font in una sezione Carattere di una forma che contiene testo formattato con tale carattere. Gli ID font possono cambiare quando un documento viene aperto su sistemi diversi o quando i font vengono installati o rimossi.
### **Recupero dell'esempio di programmazione dei caratteri**
Il seguente pezzo di codice recupera le informazioni sui font dal Visio diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveFontInfo.class);

// call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir+ "RetrieveFontInfo.vsd");

for(Font font : (Iterable<Font>) diagram.getFonts())
{
    // Display information about the fonts
    System.out.println(font.getName());
}

System.out.println("Process Completed Successfully");

{{< /highlight >}}


![cose da fare:immagine_alt_testo](retrieve-visio-connectors-and-font-information_2.png)
### **Ottenere la directory dei caratteri predefinita**
Aspose.Diagram for Java API consente inoltre di ottenere il percorso predefinito della directory dei font utilizzando il metodo getDefaultFontDir() della classe Diagram. La parte di codice seguente recupera la directory dei font predefinita da Visio diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveFontInfo.class) + "Diagrams/";

// Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");

// Display font default directory
System.out.println(diagram.getDefaultFontDir());

{{< /highlight >}}

