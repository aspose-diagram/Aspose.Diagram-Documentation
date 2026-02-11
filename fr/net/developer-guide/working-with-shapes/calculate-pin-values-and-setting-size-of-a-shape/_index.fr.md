---
title: Calculer les valeurs des broches et définir la taille d'une forme
type: docs
weight: 60
url: /fr/net/calculate-pin-values-and-setting-size-of-a-shape/
description: Cette section explique comment calculer les valeurs PinX et PinY de la sous-forme avec Aspose.Diagram.
---
## **Calculer les valeurs PinX et PinY de la sous-forme**
 Si la forme est un nœud enfant de la forme de groupe, sa xform est une coordonnée relative de sa forme parent mais pas une coordonnée absolue dans le[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page). Si l'utilisateur a besoin d'obtenir la coordonnée absolue, cet exemple de code est utile.

Un point spécifié en coordonnées locales peut être converti en coordonnées parent en appliquant les transformations suivantes dans l'ordre suivant :

1. Soustrayez la valeur de la propriété LocPinX de l'élément Cell_Type de la coordonnée x.
1. Soustrayez la valeur de la propriété LocPinY du Cell_Type de la coordonnée y.
1. Mettez en miroir le point autour de l'axe des ordonnées si la valeur de la propriété FlipX de Cell_Type est égale à un.
1. Mettez en miroir le point autour de l'axe des x si la valeur de la propriété FlipY de Cell_Type est égale à un.
1. Faites pivoter le point dans le sens antihoraire autour de l'origine de la valeur de la propriété Angle de Cell_Type.
1. Ajoutez la valeur de PinX Cell_Type à la coordonnée x.
1. Ajoutez la valeur de PinY Cell_Type à la coordonnée y.
### **Calculer l'exemple de programmation PinX et PinY**
Utilisez le code suivant dans votre application .NET pour calculer les valeurs PinX et PinY d'une sous-forme à l'aide de Aspose.Diagram for .NET API.







```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a group shape by ID and page index is 0
Shape shape = diagram.Pages[0].Shapes.GetShape(795);
// Get a sub-shape of the group shape by id
Shape subShape = shape.Shapes.GetShape(794);

Matrix m = new Matrix();
// Apply the translation vector
m.Translate(-(float)subShape.XForm.LocPinX.Value, -(float)subShape.XForm.LocPinY.Value);
// Set the elements of that matrix to a rotation
m.Rotate((float)subShape.XForm.Angle.Value);
// Apply the translation vector
m.Translate((float)subShape.XForm.PinX.Value, (float)subShape.XForm.PinY.Value);

// Get pinx and piny
double pinx = m.OffsetX;
double piny = m.OffsetY;
// Calculate the sub-shape pinx and piny
double resultx = shape.XForm.PinX.Value - shape.XForm.LocPinX.Value - pinx;
double resulty = shape.XForm.PinY.Value - shape.XForm.LocPinY.Value - piny;

{{< /highlight >}}
```
## **Définition de la hauteur et de la largeur d'une forme**
 La[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe vous permet de contrôler la taille de la forme en spécifiant la hauteur et la largeur de la forme à l'aide des méthodes SetHeight et SetWidth.

 Les méthodes SetHeight et SetWidth, exposées par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)classe, prend en charge le redimensionnement d'une forme avec le maître, sans le maître ou sous la forme d'une forme de groupe. Les exemples de code de cet article définissent la hauteur et la largeur pour redimensionner la forme sur la page.

Le processus de définition de la hauteur et de la largeur est le suivant :

1. Charger un diagram.
1. Trouvez une forme particulière.
1. Définir la hauteur d'une forme.
1. Définissez la largeur d'une forme.
1. Enregistrez le diagram.
### **Réglage de la hauteur et de la largeur Exemple de programmation**
L'extrait de code ci-dessous montre comment définir la hauteur et la largeur de la forme. Le code recherche un rectangle de nom de forme, avec l'ID de forme 1, et définit sa hauteur et sa largeur sur double.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(796);
// Alter the size of Shape
shape.SetWidth(2 * shape.XForm.Width.Value);
shape.SetHeight(2 * shape.XForm.Height.Value);
// Save diagram
diagram.Save(dataDir + "ChangeShapeSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
