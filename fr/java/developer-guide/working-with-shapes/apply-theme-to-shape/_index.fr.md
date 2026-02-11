---
title: Appliquer le thème à la forme
type: docs
weight: 70
url: /fr/java/apply-theme-to-shape/
description: Cette section explique comment définir les propriétés du thème dans une forme visio avec Aspose.Diagram.
---
## **Définir la couleur du thème sur une forme dans Visio**
Cette rubrique explique comment les développeurs peuvent appliquer une couleur de thème à une forme à l'aide de Aspose.Diagram for Java.

Le code ci-dessous montre comment :

1. Charger un échantillon diagram.
1. obtenir une page particulière.
1. obtenir une forme particulière.
1. définir le thème de la forme.
1. enregistrer diagram
#### **Définir le thème sur une forme Exemple de programmation**
Utilisez le code suivant dans votre application Java pour définir l'apparence de la forme du type de connecteur à l'aide de Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);
// Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.getPages().getPage("Page-2");

// Add master with stencil file path and master name
String masterName = "Rectangle";
diagram.addMaster(dataDir + "Basic Shapes.vss", masterName);

// Page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
// Add a new rectangle shape
long rectangleId = diagram.addShape(pinX, pinY, width, height, masterName, PageIndex);

// Set shape properties 
Shape rectangle = page.getShapes().getShape(rectangleId);
rectangle.getXForm().getPinX().setValue(5);
rectangle.getXForm().getPinY().setValue(5);
rectangle.setType(TypeValue.SHAPE);
rectangle.getText().getValue().add(new Txt("Aspose Diagram"));

// Apply preset theme clouds to new shape in page "Page-2"
rectangle.setPresetTheme(PresetThemeValue.CLOUDS);
rectangle.setPresetThemeVariant( PresetThemeVariantValue.VARIANT_1);
rectangle.setPresetThemeQuickStyle (PresetQuickStyleValue.VARIANT_STYLE_1);

// Apply preset theme bubble to page "Page-3"
Page page3 = diagram.getPages().getPage("Page-3");
page3.setPresetTheme( PresetThemeValue.BUBBLE);
page3.setPresetThemeVariant(PresetThemeVariantValue.VARIANT_2);
page3.setPresetThemeQuickStyle (PresetQuickStyleValue.VARIANT_STYLE_3);

diagram.save(dataDir + "ApplyThemeToNewShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

