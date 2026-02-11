---
title: Tillämpa tema på form
type: docs
weight: 70
url: /sv/java/apply-theme-to-shape/
description: Det här avsnittet förklarar hur du ställer in temaegenskaper i formen visio med Aspose.Diagram.
---
## **Ställ in temafärg till en form i Visio**
Det här ämnet utvecklar hur utvecklare kan applicera temafärg på en form med Aspose.Diagram for Java.

Koden nedan visar hur man:

1. Ladda ett prov diagram.
1. skaffa en viss sida.
1. få en speciell form.
1. ställ in temat för formen.
1. spara diagram
#### **Ställ in Tema till en form Programmeringsexempel**
Använd följande kod i din Java-applikation för att ställa in utseendet på kontakttypens form med Aspose.Diagram for Java.


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

