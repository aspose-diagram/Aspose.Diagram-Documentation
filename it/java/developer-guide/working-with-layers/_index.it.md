---
title: Lavorare con i livelli
type: docs
weight: 160
url: /it/java/working-with-layers/
---
### **Configurazione di oggetti forma con livelli**
Aspose.Diagram for Java consente di configurare oggetti forma con livelli in Microsoft Office Visio diagram. Ogni forma può appartenere a più livelli in modo che gli sviluppatori possano gestire le forme in base alle esigenze dell'utente finale.

 Il[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) L'oggetto class offre la proprietà LayerMember che consente di aggiungere/rimuovere oggetti forma a/dai livelli nel disegno Visio. Gli utenti possono gestire queste proprietà a livello di codice utilizzando Aspose.Diagram API come segue:

**Aggiungi, rimuovi e sposta oggetti forma a/da livelli di diagram.** 

![cose da fare:immagine_alt_testo](working-with-layers_1.png)

Il seguente pezzo di codice aiuta ad aggiungere, rimuovere e spostare le proprietà degli oggetti forma.
#### **Esempi di programmazione**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConfigureShapeLayers.class);
        
//call the diagram constructor to load visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
        
// iterate through the shapes
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage("Page-1").getShapes())
{
    if (shape.getName().toLowerCase() == "shape1")
    {
        //Add shape1 in first two layers. Here "0;1" are indexes of the layers
        LayerMem layer = shape.getLayerMem();
        layer.getLayerMember().setValue("0;1");
    }
    else if (shape.getName().toLowerCase() == "shape2")
    {
        //Remove shape2 from all the layers
        LayerMem layer = shape.getLayerMem();
        layer.getLayerMember().setValue("");
    }
    else if (shape.getName().toLowerCase() == "shape3")
    {
        //Add shape3 in first layer. Here "0" is index of the first layer
        LayerMem layer = shape.getLayerMem();
        layer.getLayerMember().setValue("0");
    }
}
// save diagram
diagram.save(dataDir + "ConfigureShapeLayers_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

### **Aggiungi un livello nel foglio di pagina Visio**
Aspose.Diagram for Java consente agli sviluppatori di aggiungere nuovi livelli per organizzare categorie personalizzate di forme e quindi assegnare forme a tali livelli in modo programmatico.

 Il[Raccolta livelli](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class offre il metodo add che consente di aggiungere un nuovo file[Strato](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)oggetto di classe nel disegno Visio. Gli sviluppatori possono impostare le proprietà del livello inizializzando il suo oggetto di classe.

Il seguente pezzo di codice aiuta ad aggiungere oggetti Layer.
#### **Esempi di programmazione**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddLayer.class) + "Layers/";

// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page page = diagram.getPages().getPage("Page-1");

// initialize a new Layer class object
Layer layer = new Layer();
// set Layer name
layer.getName().setValue("Layer1");
// set Layer Visibility
layer.getVisible().setValue(BOOL.TRUE);
// set the color checkbox of Layer
layer.setColorChecked(BOOL.TRUE);
// add Layer to the particular page sheet
page.getPageSheet().getLayers().add(layer);

// get shape by ID
Shape shape = page.getShapes().getShape(3);
// assign shape to this new Layer
shape.getLayerMem().getLayerMember().setValue(Integer.toString(layer.getIX()));
// save diagram
diagram.save(dataDir + "AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}} 

Aspose.Diagram for Java offre agli sviluppatori l'accesso ai livelli esistenti di Visio diagram.

{{% /alert %}} 
### **Ottieni tutti i livelli disponibili**
 Il[PaginaFoglio](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) proprietà del[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class consente di recuperare l'elenco dei livelli disponibili dal Visio diagram utilizzando[Raccolta livelli](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) classe.

Il seguente pezzo di codice aiuta a ottenere l'elenco dei livelli.
#### **Esempi di programmazione**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveAllLayers.class);  
// load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page page = diagram.getPages().getPage("Page-1");

// iterate through the layers
for (Layer layer : (Iterable<Layer>) page.getPageSheet().getLayers())
{
    System.out.println("Name: " + layer.getName().getValue());
    System.out.println("Visibility: " + layer.getVisible().getValue());
    System.out.println("Status: " + layer.getStatus().getValue());
}

{{< /highlight >}}

