---
title: Arbeiten mit Ebenen
type: docs
weight: 160
url: /de/java/working-with-layers/
---
### **Konfigurieren von Formobjekten mit Ebenen**
Aspose.Diagram for Java ermöglicht die Konfiguration von Formobjekten mit Ebenen in Microsoft Office Visio diagram. Jede Form kann zu mehreren Ebenen gehören, sodass Entwickler Formen verwalten können, die den Anforderungen des Endbenutzers entsprechen.

 Das[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) Das Klassenobjekt bietet die LayerMember-Eigenschaft, mit der Formobjekte zu den Ebenen in der Visio-Zeichnung hinzugefügt / entfernt werden können. Benutzer können diese Eigenschaften programmgesteuert mit Aspose.Diagram API wie folgt verwalten:

**Hinzufügen, Entfernen und Verschieben von Formobjekten zu / von Ebenen des diagram.** 

![todo: Bild_alt_Text](working-with-layers_1.png)

Der folgende Codeabschnitt hilft beim Hinzufügen, Entfernen und Verschieben von Formobjekteigenschaften.
#### **Programmierbeispiele**
```
{{< highlight "java" >}}
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
```
### **Fügen Sie eine Ebene im PageSheet Visio hinzu**
Aspose.Diagram for Java ermöglicht es Entwicklern, neue Ebenen hinzuzufügen, um benutzerdefinierte Kategorien von Formen zu organisieren, und diesen Ebenen dann programmgesteuert Formen zuzuweisen.

 Das[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) Die Klasse bietet die Methode add an, mit der Sie eine neue hinzufügen können[Schicht](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)Klassenobjekt in der Zeichnung Visio. Entwickler können Layer-Eigenschaften festlegen, indem sie ihr Klassenobjekt initialisieren.

Der folgende Codeabschnitt hilft beim Hinzufügen von Layer-Objekten.
#### **Programmierbeispiele**
```
{{< highlight "java" >}}
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
```

{{% alert color="primary" %}} 

Aspose.Diagram for Java gibt Entwicklern Zugriff auf die bestehenden Schichten von Visio diagram.

{{% /alert %}} 
### **Holen Sie sich alle verfügbaren Ebenen**
 Das[Seitenblatt](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) Eigentum der[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) Klasse ermöglicht das Abrufen der Liste der verfügbaren Layer aus der Visio diagram mit[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) Klasse.

Der folgende Codeabschnitt hilft, eine Liste der Ebenen zu erhalten.
#### **Programmierbeispiele**
```
{{< highlight "java" >}}
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
```
