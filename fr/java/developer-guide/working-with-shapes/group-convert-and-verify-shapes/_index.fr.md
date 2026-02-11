---
title: Grouper, convertir et vérifier des formes
type: docs
weight: 50
url: /fr/java/group-convert-and-verify-shapes/
---
## **Regrouper plusieurs formes dans le dessin Visio**
Aspose.Diagram API permet aux développeurs de regrouper des formes pour les déplacer toutes en même temps. Chaque forme d'un groupe conserve une identité unique et possède son propre ensemble de propriétés. Lorsque nous modifions la mise en forme d'un groupe de formes, il attribue la nouvelle propriété à chaque forme.
### **Comment grouper des formes**
La méthode Group exposée par la classe ShapeCollection peut être utilisée pour regrouper des formes.

Le code ci-dessous montre comment :

1. Charger un échantillon diagram.
1. initialisé un tableau des formes
1. obtenir une forme particulière par identifiant.
1. obtenir une autre forme particulière particulière par identifiant.
1. affecter des formes au tableau.
1. groupez des formes en appelant la méthode Group.
1. enregistrer diagram
#### **Exemple de programmation de formes de groupe**
Utilisez le code suivant dans votre application Java pour regrouper les formes en utilisant Aspose.Diagram for Java API.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GroupShapes.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// Initialize an array of shapes
Shape[] ss = new Shape[3];

// extract and assign shapes to the array
ss[0] = page.getShapes().getShape(15);
ss[1] = page.getShapes().getShape(16);
ss[2] = page.getShapes().getShape(17);

// mark array shapes as group
page.getShapes().group(ss);

// save visio diagram
diagram.save(dataDir + "GroupShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Convertir une forme Visio en d'autres formats de fichier**
Aspose.Diagram for Java API permet aux développeurs de convertir une seule forme Visio en tout autre format de fichier pris en charge. Dans cet article, nous supprimons toutes les autres formes Visio de la page et personnalisons le paramètre de page en fonction de la taille de la forme source.
### **Conversion d'une forme particulière Visio**
Developers can convert a Visio shape to PDF, HTML, Image, SVG, and SWF by [spécifiant les options de sauvegarde Visio]().
Cet exemple de code fonctionne comme suit :

1. Charger une source Visio.
1. Obtenir une page particulière.
1. Supprimez la page d'arrière-plan.
1. Construisez une table de hachage de toutes les formes contenant les identifiants et les noms.
1. Itérer dans la table de hachage
1. Supprimez toutes les formes de la page Visio, sauf celle en particulier.
1. Définissez la taille de la page.
1. Enregistrez la page Visio dans n'importe quel format de fichier pris en charge.
#### **Exemple de programmation de conversion de forme**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SaveVisioShapeInOtherFormats.class);   
        
double shapeWidth = 0;
double shapeHeight = 0;

// call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page srcPage = srcVisio.getPages().get(1);
// remove background page
srcPage.setBackPage(null);

// get hash table of shapes, it holds id and name
Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
for (Shape shape : (Iterable<Shape>)srcPage.getShapes())
    // for the normal shape
    remShapes.put(shape.getID(), shape.getName());
        

// iterate through the hash table
Enumeration<Long> enumKey = remShapes.keys();
while(enumKey.hasMoreElements())
{
    Long key = enumKey.nextElement();
    String val = remShapes.get(key);
    Shape shape = srcPage.getShapes().getShape(key);
    // check of the shape name
    if(val.equals("GroupShape1"))
    {
        // move shape to the origin corner
        shapeWidth = shape.getXForm().getWidth().getValue();
        shapeHeight = shape.getXForm().getHeight().getValue();
        shape.moveTo(shapeWidth*0.5, shapeHeight*0.5);
        // trim page size
        srcPage.getPageSheet().getPageProps().getPageWidth().setValue(shapeWidth);
        srcPage.getPageSheet().getPageProps().getPageHeight().setValue(shapeHeight);
    }
    else
    {
        // remove shape from the Visio page and hash table
        srcPage.getShapes().remove(shape);
        remShapes.remove(key);
    }
}

// specify saving options
PdfSaveOptions opts = new PdfSaveOptions();
// set page count to save
opts.setPageCount(1);
// set starting index of the page
opts.setPageIndex(1);
// save it
srcVisio.save(dataDir + "SaveVisioShapeInOtherFormats_Out.pdf", opts);

{{< /highlight >}}
```
### **Convert Visio Shape to PDF**
The ToPdf method of the Shape class allows to convert a shape into the PDF format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Convert Visio Shape to HTML**
The ToHTML method of the Shape class allows to convert a shape into the HTML format.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 Nous accueillons vos questions et suggestions à[Aspose.DiagramForum](https://forum.aspose.com/c/diagram/17). Nous vous répondrons rapidement.

{{% /alert %}} 
## **Vérifiez si deux formes Visio sont connectées ou collées**
 Aspose.Diagram for Java API permet aux développeurs de vérifier que les deux formes Visio sont collées ou connectées. Auparavant, nous avons vu comment connecter ou coller deux formes dans ces rubriques d'aide :[Ajouter et connecter des formes Visio](/diagram/fr/java/add-and-connect-visio-shapes/) et[Formes de colle à l'intérieur du conteneur](/diagram/fr/java/working-with-shapes-gluing/).
### **Vérification des formes connectées ou collées**
 La[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La classe offre les propriétés IsGlued et IsConnected pour déterminer si deux formes sont collées ou connectées.
#### **Exemple de programmation de vérification de formes connectées ou collées**
Le morceau de code suivant vérifie si deux formes sont connectées ou collées.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VerifyConnectedOrGluedShapes.class);  
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// get Visio page by name
Page page = diagram.getPages().getPage("Page-3");

// get Visio shapes by ids
Shape ShapedOne = page.getShapes().getShape(ShapeIdOne);
Shape ShapedTwo = page.getShapes().getShape(ShapeIdTwo);

// determine whether shapes are connected
boolean connected = ShapedOne.isConnected(ShapedTwo);
System.out.println("Shapes are connected: " + connected);

// determine whether shapes are glued
boolean glued = ShapedOne.isGlued(ShapedTwo);
System.out.println("Shapes are Glued: " + glued);

{{< /highlight >}}
```
## **Vérifiez si la forme Visio se trouve dans un groupe de formes**
Aspose.Diagram for Java API permet aux développeurs de vérifier que la forme Visio est dans un groupe de formes ou non.
### **Vérification de la forme dans le groupe de formes**
La classe Shape propose des propriétés IsInGroup pour déterminer si la forme Visio est dans une forme de groupe.
#### **Vérification de la forme dans l'exemple de programmation du groupe de formes**
Le morceau de code suivant vérifie si la forme est dans une forme de groupe.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
				
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
System.out.println("Is it in a Group: " + shape.isInGroup());
{{< /highlight >}}
```

{{% alert color="primary" %}} 

 Nous accueillons vos questions et suggestions à[Aspose.DiagramForum](https://forum.aspose.com/c/diagram/17). Nous vous répondrons rapidement.

{{% /alert %}}
