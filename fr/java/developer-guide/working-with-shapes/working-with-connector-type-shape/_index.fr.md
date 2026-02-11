---
title: Travailler avec la forme du type de connecteur
type: docs
weight: 80
url: /fr/java/working-with-connector-type-shape/
---
## **Définir l'apparence de la forme du type de connecteur dans Visio**
Cette rubrique explique comment les développeurs peuvent modifier l'apparence de la forme du type de connecteur dynamique à l'aide de Aspose.Diagram for Java.
### **Définir l'apparence du connecteur**
 La méthode SetConnectorsType exposée par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La classe peut être utilisée pour définir l'apparence de la forme du type de connecteur.

Le code ci-dessous montre comment :

1. Charger un échantillon diagram.
1. obtenir une page particulière.
1. obtenir une forme de connecteur particulière.
1. définir l'apparence de la forme.
1. enregistrer diagram
#### **Définir l'apparence du connecteur Exemple de programmation**
Utilisez le code suivant dans votre application Java pour définir l'apparence de la forme du type de connecteur à l'aide de Aspose.Diagram for Java.


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

## **Sélectionnez l'option de réacheminement de la forme du connecteur**
 La propriété ConFixedCode exposée par le[Disposition](https://reference.aspose.com/diagram/java/com.aspose.diagram/layout) class peut être utilisé pour sélectionner l'option de réacheminement. La propriété Layout, exposée par le[Forme](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) classe, sera utilisé.

|<p>**Comment sélectionner les options de réacheminement** </p><p>![tâche : image_autre_texte](http://i.imgur.com/1O70sSA.png)</p>|
|:- |
Le code ci-dessous montre comment :

1. Chargez un exemple de fichier.
1. obtenir une page particulière.
1. obtenir une forme de connecteur particulière.
1. définir les options de réacheminement.
1. enregistrer diagram.
### **Sélectionner l'exemple de programmation de l'option de réacheminement**
Utilisez le code suivant dans votre application Java pour sélectionner l'option de réacheminement de la forme du connecteur à l'aide de Aspose.Diagram for Java.


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

