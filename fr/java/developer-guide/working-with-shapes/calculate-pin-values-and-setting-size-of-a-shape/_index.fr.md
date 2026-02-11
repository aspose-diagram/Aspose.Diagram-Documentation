---
title: Calculer les valeurs des broches et définir la taille d'une forme
type: docs
weight: 40
url: /fr/java/calculate-pin-values-and-setting-size-of-a-shape/
---
## **Calculer les valeurs PinX et PinY de la sous-forme**
 Si la forme est un enfant de la forme du groupe, c'est xform est une coordonnée relative de sa forme parent, mais pas une coordonnée absolue dans le[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/page). Si l'utilisateur a besoin d'obtenir la coordonnée absolue, cet exemple de code est utile.

Un point spécifié en coordonnées locales peut être converti en coordonnées parent en appliquant les transformations suivantes dans l'ordre suivant :

1. Soustrayez la valeur de la propriété LocPinX de l'élément Cell_Type de la coordonnée x.
1. Soustrayez la valeur de la propriété LocPinY du Cell_Type de la coordonnée y.
1. Mettez en miroir le point autour de l'axe des ordonnées si la valeur de la propriété FlipX de Cell_Type est égale à un.
1. Mettez en miroir le point autour de l'axe des x si la valeur de la propriété FlipY de Cell_Type est égale à un.
1. Faites pivoter le point dans le sens antihoraire autour de l'origine de la valeur de la propriété Angle de Cell_Type.
1. Ajoutez la valeur de PinX Cell_Type à la coordonnée x.
1. Ajoutez la valeur de PinY Cell_Type à la coordonnée y.
### **Calculer l'exemple de programmation PinX et PinY**
Utilisez le code suivant dans votre application Java pour calculer les valeurs PinX et PinY d'une sous-forme à l'aide de Aspose.Diagram for Java API.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CalculateCenterOfSubShapes.class);
        
// load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get group shape
Shape shape = diagram.getPages().get(0).getShapes().getShape(138);
// get sub-shape of the group shape
Shape subShape = shape.getShapes().getShape(140);


AffineTransform m = new AffineTransform();
// apply the translation vector
m.translate(-(float)subShape.getXForm().getLocPinX().getValue(), -(float)subShape.getXForm().getLocPinY().getValue());		
// set the elements of that matrix to a rotation
m.rotate((float)subShape.getXForm().getAngle().getValue());
// apply the translation vector
m.translate((float)subShape.getXForm().getPinX().getValue(), (float)subShape.getXForm().getPinY().getValue());

// get pinx and piny		
double pinx = m.getTranslateX();
double piny = m.getTranslateY();
		
// calculate the sub-shape pinx and piny
double resultx = shape.getXForm().getPinX().getValue() - shape.getXForm().getLocPinX().getValue() - pinx;
double resulty = shape.getXForm().getPinY().getValue() - shape.getXForm().getLocPinY().getValue() - piny;

{{< /highlight >}}
```
## **Définition de la hauteur et de la largeur d'une forme**
 La[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La classe vous permet de contrôler la taille de la forme en spécifiant la hauteur et la largeur de la forme à l'aide des méthodes SetHeight et SetWidth.

 Les méthodes SetHeight et SetWidth, exposées par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)classe, prend en charge le redimensionnement d'une forme avec le maître, sans le maître ou sous la forme d'une forme de groupe.

Les exemples de code de cet article définissent la hauteur et la largeur pour redimensionner la forme sur la page.

**Entrée diagram** 

![tâche : image_autre_texte](http://i.imgur.com/cTiNWa7.png)

**Le diagram après la modification de la hauteur et de la largeur**

![tâche : image_autre_texte](calculate-pin-values-and-setting-size-of-a-shape_1.png)

Le processus de définition de la hauteur et de la largeur est le suivant :

1. Charger un diagram.
1. Trouvez une forme particulière.
1. Définir la hauteur d'une forme.
1. Définissez la largeur d'une forme.
1. Enregistrez le diagram.
### **Réglage de la hauteur et de la largeur Exemple de programmation**
L'extrait de code ci-dessous montre comment définir la hauteur et la largeur de la forme. Le code recherche un rectangle de nom de forme, avec l'ID de forme 1, et définit sa hauteur et sa largeur sur double.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeShapeSize.class);
        
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(796);
// alter the size of Shape
shape.setWidth(2 * shape.getXForm().getWidth().getValue());
shape.setHeight(2 * shape.getXForm().getHeight().getValue());
// save diagram
diagram.save(dataDir + "ChangeShapeSize_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
