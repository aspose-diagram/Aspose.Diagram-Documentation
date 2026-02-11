---
title: Arbeta med teman
type: docs
weight: 265
url: /sv/net/working-with-themes/
description: Det här avsnittet förklarar hur du tillämpar ett förinställt tema på en sida eller en form med Aspose.Diagram.
---
## **Hur man applicerar ett förinställt tema på en sida eller en form**
Den här artikeln kan vara användbar för alla som vill ändra temat för en givande VSDX-fil med Aspose.Diagram. Vi använder en testfil Themes1.vsdx, se ut som nedan.

|**Tema1.vsdx**|
|:- |
|![Tema1.vsdx](theme1.png)|

### **Tillämpa ett förinställt tema på en sida**
Aspose.Diagram API:er gör det möjligt att tillämpa ett förinställt tema för att få ett enhetligt utseende och känsla på former på en sida och över flera dokument. Utför följande steg för att göra detta:

- Skapa en instans av klassen Diagram för att ladda en diagram
- Skaffa en instans av Sidklass som ska ställas in
- Tilldela ett förinställt värde till egenskapen PresetTheme för Page-instansen
#### **Tillämpa ett förinställt tema på ett sidprogrammeringsexempel**
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

|**Resultat av att tillämpa ett förinställt tema på en sida**|
|:- |
|![SetTheme_out.vsdx](theme2.png)|

### **Tillämpa en förinställd temavariant på en sida**

Aspose.Diagram API: er gör det möjligt att tillämpa en förinställd temavariant för att få ett enhetligt utseende och känsla för former på en sida och över flera dokument. Utför följande steg för att göra detta:

- Skapa en instans av klassen Diagram för att ladda en diagram
- Skaffa en instans av Sidklass som ska ställas in
- Tilldela ett förinställt värde till egenskapen PresetTheme för Page-instansen
- Tilldela ett förinställt värde till egenskapen PresetThemeVariant för Page-instansen

#### **Tillämpa en förinställd temavariant på ett sidprogrammeringsexempel**

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

|**Resultat av att tillämpa en förinställd temavariant på en sida**|
|:- |
|![SetTheme_out.vsdx](theme3.png)|

### **Tillämpa ett förinställt tema på en form**

Aspose.Diagram API:er gör det möjligt att tillämpa ett förinställt tema på en form på en sida. Utför följande steg för att göra detta:

- Skapa en instans av klassen Diagram för att ladda en diagram
- Skaffa en instans av Shape class som ska ställas in tema
- Tilldela ett förinställt värde till egenskapen PresetTheme för Shape-instansen

#### **Tillämpa ett förinställt tema på ett formprogrammeringsexempel**

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

|**Resultatet av att tillämpa ett förinställt tema på en form**|
|:- |
|![SetTheme_out.vsdx](theme4.png)|

### **Applicera en förinställd temavariant på en form**

Aspose.Diagram API:er gör det möjligt att tillämpa en förinställd temavariant på en form på en sida. Utför följande steg för att göra detta:

- Skapa en instans av klassen Diagram för att ladda en diagram
- Skaffa en instans av Shape class som ska ställas in tema
- Tilldela ett förinställt värde till egenskapen PresetTheme för Shape-instansen
- Tilldela ett förinställt värde till egenskapen PresetThemeVariant för Shape-instansen

#### **Tillämpa en förinställd temavariant på ett formprogrammeringsexempel**

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

|**Resultat av att tillämpa en förinställd temavariant på en form**|
|:- |
|![SetTheme_out.vsdx](theme5.png)|

### **Tillämpa en förinställd temavariant Quickstyle på en form**

Aspose.Diagram API:er gör det möjligt att tillämpa ett förinställt tema quickstyle på en form på en sida. Utför följande steg för att göra detta:

- Skapa en instans av klassen Diagram för att ladda en diagram
- Skaffa en instans av Shape class som ska ställas in tema
- Tilldela ett förinställt värde till egenskapen PresetTheme för Shape-instansen
- Tilldela ett förinställt värde till egenskapen PresetThemeVariant för Shape-instansen
- Tilldela ett förinställt värde till egenskapen PresetThemeQuickStyle för Shape-instansen

#### **Tillämpa en förinställd temavariant Quickstyle på ett formprogrammeringsexempel**

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

|**Resultat av att tillämpa en förinställd temavariant Quickstyle på en form**|
|:- |
|![SetTheme_out.vsdx](theme6.png)|

### **Tillämpa en förinställd temastil på en form med metoden SetPresetThemeStyleMatrics**

Aspose.Diagram API:er gör det möjligt att tillämpa ett förinställt tema quickstyle på en form på en sida. Utför följande steg för att göra detta:

- Skapa en instans av klassen Diagram för att ladda en diagram
- Skaffa en instans av Shape class som ska ställas in tema
- Tilldela ett förinställt värde till egenskapen PresetTheme för Shape-instansen
- Tilldela ett förinställt värde till egenskapen PresetThemeVariant för Shape-instansen
- Tilldela en temastil genom att ställa in stilvärde och färgvärde för Shape-instansen med metoden SetPresetThemeStyleMatrics

#### **Tillämpa en förinställd temastil på en form med hjälp av SetPresetThemeStyleMatrics Method Programmeringsexempel**

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

|**Resultat av att tillämpa en förinställd temastil på en form med metoden SetPresetThemeStyleMatrics**|
|:- |
|![SetTheme_out.vsdx](theme7.png)|
