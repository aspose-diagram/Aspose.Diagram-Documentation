---
title: Trabajar con temas
type: docs
weight: 265
url: /es/java/working-with-themes/
description: Esta sección explica cómo aplicar un tema predeterminado a una página o una forma con Aspose.Diagram.
---
## **Cómo aplicar un tema preestablecido a una página o una forma**
Este artículo puede ser útil para cualquier persona que quiera modificar el tema de un archivo de VSDX dando usando Aspose.Diagram. Usamos un archivo de prueba Themes1.vsdx, como se muestra a continuación.

|**Tema1.vsdx**|
|:- |
|![Tema1.vsdx](theme1.png)|

### **Aplicar un tema preestablecido a una página**
Aspose.Diagram Las API permiten aplicar un tema preestablecido para obtener una apariencia uniforme para las formas dentro de una página y en varios documentos. Realice los siguientes pasos para hacer esto:

- Cree una instancia de la clase Diagram para cargar un diagram
- Obtenga una instancia de la clase de página para establecer el tema
- Asigne un valor preestablecido a la propiedad PresetTheme de la instancia de página
#### **Aplicar un tema preestablecido a una muestra de programación de página**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioThemes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Page class to be set theme
Page page = diagram.getPages().get(0);
//Assign a Preset value to the PresetTheme property of the Page instance
page.setPresetTheme(PresetThemeValue.BUBBLE);
// Save diagram
diagram.save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


|**Resultado de aplicar un tema preestablecido a una página**|
|:- |
|![SetTheme_out.vsdx](theme2.png)|

### **Aplicar una variante de tema preestablecido a una página**

Aspose.Diagram Las API permiten aplicar una variante de tema preestablecido para obtener una apariencia uniforme para las formas dentro de una página y en varios documentos. Realice los siguientes pasos para hacer esto:

- Cree una instancia de la clase Diagram para cargar un diagram
- Obtenga una instancia de la clase de página para establecer el tema
- Asigne un valor preestablecido a la propiedad PresetTheme de la instancia de página
- Asigne un valor preestablecido a la propiedad PresetThemeVariant de la instancia de página

#### **Aplicar una variante de tema preestablecido a una muestra de programación de página**


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioThemes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Page class to be set theme
Page page = diagram.getPages().get(0);
//Assign a Preset value to the PresetTheme property of the Page instance
page.setPresetTheme(PresetThemeValue.BUBBLE);
//Assign a Preset value to the PresetThemeVariant property of the Page instance
page.setPresetThemeVariant(PresetThemeVariantValue.VARIANT_3);
// Save diagram
diagram.save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}


|**Resultado de aplicar una variante de tema preestablecido a una página**|
|:- |
|![SetTheme_out.vsdx](theme3.png)|

### **Aplicar un tema preestablecido a una forma**

Aspose.Diagram Las API permiten aplicar un tema preestablecido a una forma dentro de una página. Realice los siguientes pasos para hacer esto:

- Cree una instancia de la clase Diagram para cargar un diagram
- Obtenga una instancia de la clase Shape para establecer el tema
- Asigne un valor preestablecido a la propiedad PresetTheme de la instancia de Shape

#### **Aplicar un tema preestablecido a una muestra de programación de formas**


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioThemes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.getPages().get(0).getShapes().get(0);
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.setPresetTheme(PresetThemeValue.BUBBLE);
// Save diagram
diagram.save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}


|**Resultado de aplicar un tema preestablecido a una forma**|
|:- |
|![SetTheme_out.vsdx](theme4.png)|

### **Aplicar una variante de tema preestablecido a una forma**

Aspose.Diagram Las API permiten aplicar una variante de tema preestablecido a una forma dentro de una página. Realice los siguientes pasos para hacer esto:

- Cree una instancia de la clase Diagram para cargar un diagram
- Obtenga una instancia de la clase Shape para establecer el tema
- Asigne un valor preestablecido a la propiedad PresetTheme de la instancia de Shape
- Asigne un valor preestablecido a la propiedad PresetThemeVariant de la instancia de Shape

#### **Aplicar una variante de tema preestablecido a una muestra de programación de forma**


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioThemes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.getPages().get(0).getShapes().get(0);
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.setPresetTheme(PresetThemeValue.BUBBLE);
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.setPresetThemeVariant(PresetThemeVariantValue.VARIANT_3);
// Save diagram
diagram.save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}


|**Resultado de aplicar una variante de tema preestablecido a una forma**|
|:- |
|![SetTheme_out.vsdx](theme5.png)|

### **Aplicar una variante de tema preestablecido Quickstyle a una forma**

Aspose.Diagram Las API permiten aplicar un estilo rápido de tema preestablecido a una forma dentro de una página. Realice los siguientes pasos para hacer esto:

- Cree una instancia de la clase Diagram para cargar un diagram
- Obtenga una instancia de la clase Shape para establecer el tema
- Asigne un valor preestablecido a la propiedad PresetTheme de la instancia de Shape
- Asigne un valor preestablecido a la propiedad PresetThemeVariant de la instancia de Shape
- Asigne un valor preestablecido a la propiedad PresetThemeQuickStyle de la instancia de Shape

#### **Aplicar una variante de tema preestablecido Quickstyle a una muestra de programación de forma**


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioThemes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.getPages().get(0).getShapes().get(0);
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.setPresetTheme(PresetThemeValue.BUBBLE);
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.setPresetThemeVariant(PresetThemeVariantValue.VARIANT_3);
//Assign a Preset value to the PresetThemeQuickStyle property of the Shape instance
shape.setPresetThemeQuickStyle(PresetQuickStyleValue.VARIANT_STYLE_2);
// Save diagram
diagram.save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}


|**Resultado de aplicar un estilo rápido de variante de tema preestablecido a una forma**|
|:- |
|![SetTheme_out.vsdx](theme6.png)|

### **Aplicar un estilo de tema preestablecido a una forma mediante el método SetPresetThemeStyleMatrics**

Aspose.Diagram Las API permiten aplicar un estilo rápido de tema preestablecido a una forma dentro de una página. Realice los siguientes pasos para hacer esto:

- Cree una instancia de la clase Diagram para cargar un diagram
- Obtenga una instancia de la clase Shape para establecer el tema
- Asigne un valor preestablecido a la propiedad PresetTheme de la instancia de Shape
- Asigne un valor preestablecido a la propiedad PresetThemeVariant de la instancia de Shape
- Asigne un estilo de tema configurando el valor de estilo y el valor de color de la instancia de Shape usando el método setPresetThemeStyleMatrics

#### **Aplicar un estilo de tema preestablecido a una forma mediante el ejemplo de programación del método setPresetThemeStyleMatrics**


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioThemes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.getPages().get(0).getShapes().get(0);
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.setPresetTheme(PresetThemeValue.BUBBLE);
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.setPresetThemeVariant(PresetThemeVariantValue.VARIANT_3);
//Assign a theme style by setting style value and color value of the Shape instance
shape.setPresetThemeStyleMatrics(PresetStyleMatricsValue.STYLE_2, PresetColorMatricsValue.COLOR_7);
// Save diagram
diagram.save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}


|**Resultado de aplicar un estilo de tema preestablecido a una forma mediante el método setPresetThemeStyleMatrics** |
|:----------------------------------------------------------- |
|![SetTheme_out.vsdx](theme7.png)                             |
