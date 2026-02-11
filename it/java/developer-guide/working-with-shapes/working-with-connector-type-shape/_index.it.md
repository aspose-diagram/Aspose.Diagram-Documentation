---
title: Utilizzo della forma del tipo di connettore
type: docs
weight: 80
url: /it/java/working-with-connector-type-shape/
---
## **Impostare l'aspetto della forma del tipo di connettore in Visio**
Questo argomento illustra in che modo gli sviluppatori possono modificare l'aspetto della forma del tipo di connettore dinamico utilizzando Aspose.Diagram for Java.
### **Imposta l'aspetto del connettore**
 Il metodo SetConnectorsType esposto da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class può essere utilizzata per impostare l'aspetto della forma del tipo di connettore.

Il codice seguente mostra come:

1. Carica un campione diagram.
1. ottenere una pagina particolare.
1. ottenere una particolare forma del connettore.
1. impostare l'aspetto della forma.
1. salvo diagram
#### **Esempio di programmazione dell'aspetto del connettore**
Utilizzare il seguente codice nell'applicazione Java per impostare l'aspetto della forma del tipo di connettore utilizzando Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetConnectorAppearance.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//get a particular page
Page page = diagram.getPages().getPage("Page-3");
//get a dynamic connector type shape by id
Shape shape = page.getShapes().getShape(18);
// set dynamic connector appearance
shape.setConnectorsType(ConnectorsTypeValue.STRAIGHT_LINES);

//saving Visio diagram
diagram.save(dataDir + "SetConnectorAppearance_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Selezionare l'opzione di reindirizzamento della forma del connettore**
 La proprietà ConFixedCode esposta da[Disposizione](https://reference.aspose.com/diagram/java/com.aspose.diagram/layout) la classe può essere utilizzata per selezionare l'opzione di reinstradamento. La proprietà Layout, esposta da[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) classe, verrà utilizzato.

|<p>**Come selezionare le opzioni di reindirizzamento** </p><p>![cose da fare:immagine_alt_testo](http://i.imgur.com/1O70sSA.png)</p>|
|:- |
Il codice seguente mostra come:

1. Carica un file di esempio.
1. ottenere una pagina particolare.
1. ottenere una particolare forma del connettore.
1. impostare le opzioni di reindirizzamento.
1. salvo diagram.
### **Selezionare Esempio di programmazione dell'opzione di reindirizzamento**
Utilizzare il seguente codice nell'applicazione Java per selezionare l'opzione di reinstradamento della forma del connettore utilizzando Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RerouteConnectors.class);   
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// get a particular connector shape
Shape shape = page.getShapes().getShape(18);
// set reroute option
shape.getLayout().getConFixedCode().setValue(ConFixedCodeValue.NEVER_REROUTE);

// save Visio diagram
diagram.save(dataDir + "RerouteConnectors_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

