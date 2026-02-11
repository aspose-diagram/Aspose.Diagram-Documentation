---
title: Définir Visio les données XForm, Line et Fill de la forme
type: docs
weight: 70
url: /fr/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **Définition des données XForm**
 L'élément XForm fait partie du schéma XML Microsoft Visio. XForm spécifie une position de formes, par exemple la largeur, la hauteur, la rotation et si la forme a été retournée. La[XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) propriété, exposée par la[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) classe, prend en charge l'objet Aspose.Diagram.XForm. La propriété XForm peut être utilisée pour récupérer ou mettre à jour les données XForm d'une forme. Les exemples de code de cet article modifient les valeurs XForm PinX (coordonnée X) et PinY (coordonnée Y) pour déplacer les formes sur la page.

**Entrée diagram** 

![tâche : image_autre_texte](set-visio-shape-s-xform-line-and-fill-data_1.png)

**Le diagram après le** **PinX** **et** **PinY** **les valeurs ont été modifiées** 

![tâche : image_autre_texte](set-visio-shape-s-xform-line-and-fill-data_2.png)

Le processus de mise à jour des données XForm est :

1. Charger un diagram.# Trouver une forme particulière.# Mettre à jour les données XForm de la forme.
1. Enregistrez le diagram.
### **Exemple de programmation**
L'extrait de code ci-dessous montre comment mettre à jour les données XForm d'une forme. Le code recherche un processus de noms de forme, avec l'ID de forme 1, et définit ses coordonnées X et Y sur 5.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetXFormdata.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

//Find a particular shape and update its XForm
for(Shape shape :(Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)
    {
        shape.getXForm().getPinX().setValue(5);
        shape.getXForm().getPinY().setValue(5);
    }
}
// save diagram
diagram.save(dataDir + "SetXFormdata_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Définir les données de ligne de la forme Visio**
Les formes peuvent être formatées de plusieurs manières. Cet article explique comment spécifier les attributs d'une ligne.

Microsoft Visio permet aux utilisateurs de formater les lignes de différentes manières. Aspose.Diagram for Java prend en charge :

- Poids : l'épaisseur d'une ligne.
- Couleur : définissez la couleur de la ligne de la forme.
- Transparence de la couleur de la ligne : définissez la transparence de la couleur de la ligne de la forme en pourcentage.
- Motif : définit si la ligne est pleine, en pointillés ou a un autre motif.
- Arrondi : le rayon des coins.
- Flèches de début et de fin : indiquez si la ligne comporte des flèches.
- Tailles des flèches de début et de fin : définissez les tailles des flèches.
- Cap : l'arrondi de la ligne se termine.
### **Modifier la couleur de la ligne, l'épaisseur, le type de tiret, la transparence, l'arrondi, le type de flèche et la taille de la flèche de la bordure d'une forme**
 La[Ligne](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) propriété, exposée par la[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)classe, prend en charge l'objet Aspose.Diagram.Line. Cette propriété peut être utilisée pour récupérer ou mettre à jour les données de ligne d'une forme.
#### **Exemple de programmation de données de ligne**
Le morceau de code suivant met à jour les données de ligne de shape.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetLineData.class);

// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// get the page by its name
Page page1 = diagram.getPages().getPage("Page-1");
// get shape by its ID
Shape shape = page1.getShapes().getShape(1);
// set line dash type by index
shape.getLine().getLinePattern().setValue(4);
// set line weight, defualt in PT
shape.getLine().getLineWeight().setValue(2);
// set color of the shape's line
shape.getLine().getLineColor().getUfe().setF("RGB(95,108,53)");
// set line rounding, default in inch
shape.getLine().getRounding().setValue(0.3125);
// set line caps
shape.getLine().getLineCap().setValue(BOOL.TRUE);
// set line color transparency in percent
shape.getLine().getLineColorTrans().setValue(50);

/* add arrows to the connector or curve shapes */
// select arrow type by index
shape.getLine().getBeginArrow().setValue(4);
shape.getLine().getEndArrow().setValue(4);
// set arrow size 
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);

// save the Visio
diagram.save(dataDir + "SetLineData_Out.vsdx", SaveFileFormat.VSDX);
// save diagram
diagram.save(dataDir+ "output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Définir les données de remplissage de la forme Visio**
Les formes peuvent être formatées de plusieurs manières. Cette rubrique décrit comment spécifier le remplissage d'une forme.

 Microsoft Office Visio permet aux utilisateurs de formater les remplissages de différentes manières. La[Remplir](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) classe du Aspose.Diagram for Java API prend en charge le réglage :

- Couleurs de fond et de premier plan.
- Transparence.
- Motifs de remplissage.
- Ombres.
### **Définition des valeurs de remplissage**
La propriété Fill, exposée par la classe Shape, prend en charge l'objet Aspose.Diagram.Fill. La propriété Fill peut être utilisée pour récupérer ou mettre à jour les données de remplissage d'une forme.

|<p>**L'entrée diagram** </p><p>![tâche : image_autre_texte](http://i.imgur.com/OrhEecb.png)</p>|<p>**Le diagram après avoir changé la couleur de remplissage** </p><p>![tâche : image_autre_texte](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **Exemple de programmation de données de remplissage**
L'extrait de code suivant met à jour les données de remplissage d'une forme. Le code recherche une forme nommée rectangle, avec l'ID de forme 1, et définit les couleurs de remplissage d'arrière-plan et de premier plan.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetFillData.class);


//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir+ "Drawing1.vsd");

//Find a particular shape and update its XForm
for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "rectangle" && shape.getID() == 1)
    {
        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue());
        shape.getFill().getFillForegnd().setValue("#ebf8df");
    }
}
// save diagram
diagram.save(dataDir+ "SetFillData_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Récupérer les données de remplissage héritées d'une forme Visio**
Les formes Visio peuvent hériter du style parent et de la forme principale. Les développeurs peuvent obtenir ou définir les données de remplissage héritées d'une forme Visio. La propriété InheritFill, exposée par la classe Shape, contient les valeurs de formatage de remplissage pour la forme héritée par le style parent et la forme principale.
#### **Récupérer un exemple de programmation de données de remplissage héritées**
L'extrait de code suivant récupère les données de remplissage héritées de la forme. Veuillez vérifier cet exemple de code :

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}
```
