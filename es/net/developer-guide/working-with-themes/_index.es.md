---
title: Trabajar con temas
type: docs
weight: 265
url: /es/net/working-with-themes/
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

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Page class to be set theme
Page page = diagram.Pages[0];
//Assign a Preset value to the PresetTheme property of the Page instance
page.PresetTheme = PresetThemeValue.Bubble;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Page class to be set theme
Page page = diagram.Pages[0];
//Assign a Preset value to the PresetTheme property of the Page instance
page.PresetTheme = PresetThemeValue.Bubble;
//Assign a Preset value to the PresetThemeVariant property of the Page instance
page.PresetThemeVariant = PresetThemeVariantValue.Variant3;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.Pages[0].Shapes[0];
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.PresetTheme = PresetThemeValue.Bubble;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.Pages[0].Shapes[0];
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.PresetTheme = PresetThemeValue.Bubble;
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.PresetThemeVariant = PresetThemeVariantValue.Variant3;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.Pages[0].Shapes[0];
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.PresetTheme = PresetThemeValue.Bubble;
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.PresetThemeVariant = PresetThemeVariantValue.Variant3;
//Assign a Preset value to the PresetThemeQuickStyle property of the Shape instance
shape.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle2;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
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
- Asigne un estilo de tema configurando el valor de estilo y el valor de color de la instancia de Shape usando el método SetPresetThemeStyleMatrics

#### **Aplicar un estilo de tema preestablecido a una forma usando el ejemplo de programación del método SetPresetThemeStyleMatrics**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.Pages[0].Shapes[0];
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.PresetTheme = PresetThemeValue.Bubble;
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.PresetThemeVariant = PresetThemeVariantValue.Variant3;
//Assign a theme style by setting style value and color value of the Shape instance
shape.SetPresetThemeStyleMatrics(PresetStyleMatricsValue.Style2, PresetColorMatricsValue.Color7);
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}


|**Resultado de aplicar un estilo de tema preestablecido a una forma mediante el método SetPresetThemeStyleMatrics**|
|:- |
|![SetTheme_out.vsdx](theme7.png)|
