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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveConnectorInfo-RetrieveConnectorInfo.cs" >}}
## **Recupero delle informazioni sui caratteri**
 Aspose.Diagram dispone di meccanismi per recuperare informazioni sugli elementi che compongono un diagram, da[pagine](/diagram/it/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [stencil](https://docs.aspose.com/diagram/net/working-with-masters/), [connettori](/diagram/it/net/retrieving-connector-information/) anche i caratteri. Questo articolo mostra come scoprire quali caratteri sono utilizzati in un diagram.

 Il[Font](http://www.aspose.com/api/net/diagram/aspose.diagram/font) oggetto rappresenta un carattere tipografico applicato al testo in un documento o disponibile per l'uso nel sistema. Un oggetto Font associa un nome (ad esempio, "Arial") all'ID del carattere (ad esempio, 3) che Microsoft Visio memorizza in una cella Font in una sezione Carattere di una forma che contiene testo formattato con tale carattere. Gli ID font possono cambiare quando un documento viene aperto su sistemi diversi o quando i font vengono installati o rimossi.
### **Recupero dell'esempio di programmazione dei caratteri**
Il seguente pezzo di codice recupera le informazioni sui font dal Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveFontInfo-RetrieveFontInfo.cs" >}}
### **Ottenere la directory dei caratteri predefinita**
Aspose.Diagram for .NET API consente inoltre di ottenere il percorso predefinito della directory dei caratteri utilizzando il metodo GetDefaultFontDir() della classe Diagram. La parte di codice seguente recupera la directory dei font predefinita da Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-GetDefaultFontDirectory-GetDefaultFontDirectory.cs" >}}
### **Ottenere caratteri inutilizzati**
{{% alert color="primary" %}}

Questo metodo è supportato dalla versione 19.6 o successiva.

{{% /alert %}}

Aspose.Diagram for .NET API consente inoltre di ottenere font inutilizzati utilizzando il metodo GetUnusedStyles() della classe Diagram. Il seguente pezzo di codice recupera i caratteri inutilizzati dal Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-GetUnusedFonts-1.cs" >}}
