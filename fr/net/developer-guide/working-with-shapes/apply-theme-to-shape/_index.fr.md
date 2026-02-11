---
title: Appliquer le thème à la forme
type: docs
weight: 70
url: /fr/net/apply-theme-to-shape/
description: Cette section explique comment définir les propriétés du thème dans une forme visio avec Aspose.Diagram.
---
## **Définir la couleur du thème sur une forme dans Visio**
Cette rubrique explique comment les développeurs peuvent appliquer une couleur de thème à une forme à l'aide de Aspose.Diagram for .NET.

Le code ci-dessous montre comment :

1. Charger un échantillon diagram.
1. obtenir une page particulière.
1. obtenir une forme particulière.
1. définir le thème de la forme.
1. enregistrer diagram
#### **Définir le thème sur une forme Exemple de programmation**
Utilisez le code suivant dans votre application .NET pour définir l'apparence de la forme du type de connecteur à l'aide de Aspose.Diagram for .NET.


{{< highlight csharp >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-2");

// Add master with stencil file path and master name
string masterName = "Rectangle";
diagram.AddMaster(dataDir + "Basic Shapes.vss", masterName);

// Page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
// Add a new rectangle shape
long rectangleId = diagram.AddShape(pinX, pinY, width, height, masterName, PageIndex);

// Set shape properties 
Shape rectangle = page.Shapes.GetShape(rectangleId);
rectangle.XForm.PinX.Value = 5;
rectangle.XForm.PinY.Value = 5;
rectangle.Type = TypeValue.Shape;
rectangle.Text.Value.Add(new Txt("Aspose Diagram"));

// Apply preset theme clouds to new shape in page "Page-2"
rectangle.PresetTheme = PresetThemeValue.Clouds;
rectangle.PresetThemeVariant = PresetThemeVariantValue.Variant1;
rectangle.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle1;

// Apply preset theme bubble to page "Page-3"
Page page3 = diagram.Pages.GetPage("Page-3");
page3.PresetTheme = PresetThemeValue.Bubble;
page3.PresetThemeVariant = PresetThemeVariantValue.Variant2;
page3.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle3;

diagram.Save(dataDir + "ApplyThemeToNewShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

