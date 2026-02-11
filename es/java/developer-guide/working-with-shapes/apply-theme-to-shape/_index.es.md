---
title: Aplicar tema a la forma
type: docs
weight: 70
url: /es/java/apply-theme-to-shape/
description: Esta sección explica cómo configurar las propiedades del tema en una forma visio con Aspose.Diagram.
---
## **Establecer el color del tema en una forma en Visio**
Este tema explica cómo los desarrolladores pueden aplicar el color del tema a una forma usando Aspose.Diagram for Java.

El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. obtener una página en particular.
1. obtener una forma particular.
1. establecer el tema de la forma.
1. guardar diagram
#### **Establecer el tema en una forma Ejemplo de programación**
Use el siguiente código en su aplicación Java para establecer la apariencia de la forma del tipo de conector usando Aspose.Diagram for Java.


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

