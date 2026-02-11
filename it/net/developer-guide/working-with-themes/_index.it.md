---
title: Lavorare con i temi
type: docs
weight: 265
url: /it/net/working-with-themes/
description: Questa sezione spiega come applicare un tema preimpostato a una pagina o una forma con Aspose.Diagram.
---
## **Come applicare un tema preimpostato a una pagina o a una forma**
Questo articolo può essere utile a chiunque desideri modificare il tema di un file VSDX utilizzando Aspose.Diagram. Utilizziamo un file di prova Themes1.vsdx, come di seguito.

|**Tema1.vsdx**|
|:- |
|![Tema1.vsdx](theme1.png)|

### **Applicare un tema preimpostato a una pagina**
Aspose.Diagram Le API consentono di applicare un tema preimpostato per ottenere un aspetto uniforme delle forme all'interno di una pagina e su più documenti. Eseguire i seguenti passaggi per fare ciò:

- Crea un'istanza della classe Diagram per caricare un diagram
- Ottieni un'istanza della classe Page da impostare come tema
- Assegnare un valore Preset alla proprietà PresetTheme dell'istanza Page
#### **Applicare un tema preimpostato a un esempio di programmazione della pagina**
```
{{< highlight "csharp" >}}
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
```

|**Risultato dell'applicazione di un tema preimpostato a una pagina**|
|:- |
|![SetTheme_out.vsdx](theme2.png)|

### **Applicare una variante del tema preimpostato a una pagina**

Le API Aspose.Diagram consentono di applicare una variante del tema preimpostata per ottenere un aspetto uniforme delle forme all'interno di una pagina e su più documenti. Eseguire i seguenti passaggi per fare ciò:

- Crea un'istanza della classe Diagram per caricare un diagram
- Ottieni un'istanza della classe Page da impostare come tema
- Assegnare un valore Preset alla proprietà PresetTheme dell'istanza Page
- Assegnare un valore Preset alla proprietà PresetThemeVariant dell'istanza Page

#### **Applicare una variante del tema preimpostato a un esempio di programmazione della pagina**

```
{{< highlight "csharp" >}}
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
```

|**Risultato dell'applicazione di una variante del tema preimpostato a una pagina**|
|:- |
|![SetTheme_out.vsdx](theme3.png)|

### **Applicare un tema preimpostato a una forma**

Aspose.Diagram API consente di applicare un tema preimpostato a una forma all'interno di una pagina. Eseguire i seguenti passaggi per fare ciò:

- Crea un'istanza della classe Diagram per caricare un diagram
- Ottieni un'istanza della classe Shape da impostare come tema
- Assegnare un valore Preset alla proprietà PresetTheme dell'istanza Shape

#### **Applicare un tema preimpostato a un esempio di programmazione di forme**

```
{{< highlight "csharp" >}}
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
```

|**Risultato dell'applicazione di un tema preimpostato a una forma**|
|:- |
|![SetTheme_out.vsdx](theme4.png)|

### **Applicare una variante del tema preimpostato a una forma**

Aspose.Diagram API consente di applicare una variante del tema preimpostato a una forma all'interno di una pagina. Eseguire i seguenti passaggi per fare ciò:

- Crea un'istanza della classe Diagram per caricare un diagram
- Ottieni un'istanza della classe Shape da impostare come tema
- Assegnare un valore Preset alla proprietà PresetTheme dell'istanza Shape
- Assegnare un valore Preset alla proprietà PresetThemeVariant dell'istanza Shape

#### **Applicare una variante del tema preimpostato a un esempio di programmazione di forme**

```
{{< highlight "csharp" >}}
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
```

|**Risultato dell'applicazione di una variante del tema preimpostato a una forma**|
|:- |
|![SetTheme_out.vsdx](theme5.png)|

### **Applicare uno stile rapido variante del tema preimpostato a una forma**

Aspose.Diagram API consente di applicare uno stile rapido del tema preimpostato a una forma all'interno di una pagina. Eseguire i seguenti passaggi per fare ciò:

- Crea un'istanza della classe Diagram per caricare un diagram
- Ottieni un'istanza della classe Shape da impostare come tema
- Assegnare un valore Preset alla proprietà PresetTheme dell'istanza Shape
- Assegnare un valore Preset alla proprietà PresetThemeVariant dell'istanza Shape
- Assegnare un valore Preset alla proprietà PresetThemeQuickStyle dell'istanza Shape

#### **Applicare uno stile rapido della variante del tema preimpostato a un esempio di programmazione di forme**

```
{{< highlight "csharp" >}}
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
```

|**Risultato dell'applicazione di uno stile rapido della variante del tema preimpostato a una forma**|
|:- |
|![SetTheme_out.vsdx](theme6.png)|

### **Applicare uno stile tema preimpostato a una forma utilizzando il metodo SetPresetThemeStyleMatrics**

Aspose.Diagram API consente di applicare uno stile rapido del tema preimpostato a una forma all'interno di una pagina. Eseguire i seguenti passaggi per fare ciò:

- Crea un'istanza della classe Diagram per caricare un diagram
- Ottieni un'istanza della classe Shape da impostare come tema
- Assegnare un valore Preset alla proprietà PresetTheme dell'istanza Shape
- Assegnare un valore Preset alla proprietà PresetThemeVariant dell'istanza Shape
- Assegna uno stile del tema impostando il valore dello stile e il valore del colore dell'istanza Shape usando il metodo SetPresetThemeStyleMatrics

#### **Applicare uno stile di tema preimpostato a una forma usando l'esempio di programmazione del metodo SetPresetThemeStyleMatrics**

```
{{< highlight "csharp" >}}
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
```

|**Risultato dell'applicazione di uno stile tema preimpostato a una forma utilizzando il metodo SetPresetThemeStyleMatrics**|
|:- |
|![SetTheme_out.vsdx](theme7.png)|
