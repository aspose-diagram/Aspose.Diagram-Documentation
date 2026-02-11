---
title: Travailler avec des thèmes
type: docs
weight: 265
url: /fr/java/working-with-themes/
description: Cette section explique comment appliquer un thème prédéfini à une page ou une forme avec Aspose.Diagram.
---
## **Comment appliquer un thème prédéfini à une page ou à une forme**
Cet article peut être utile à tous ceux qui souhaitent modifier le thème d'un fichier VSDX en utilisant Aspose.Diagram. Nous utilisons un fichier de test Themes1.vsdx, comme ci-dessous.

|**Thème1.vsdx**|
|:- |
|![Thème1.vsdx](theme1.png)|

### **Appliquer un thème prédéfini à une page**
Les API Aspose.Diagram permettent d'appliquer un thème prédéfini pour obtenir une apparence uniforme des formes dans une page et sur plusieurs documents. Effectuez les étapes suivantes pour ce faire :

- Créez une instance de la classe Diagram pour charger un diagram
- Obtenez une instance de la classe Page pour définir le thème
- Attribuez une valeur Preset à la propriété PresetTheme de l'instance Page
#### **Appliquer un thème prédéfini à un exemple de programmation de page**

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


|**Résultat de l'application d'un thème prédéfini à une page**|
|:- |
|![SetTheme_out.vsdx](theme2.png)|

### **Appliquer une variante de thème prédéfinie à une page**

Les API Aspose.Diagram permettent d'appliquer une variante de thème prédéfinie pour obtenir une apparence uniforme des formes dans une page et sur plusieurs documents. Effectuez les étapes suivantes pour ce faire :

- Créez une instance de la classe Diagram pour charger un diagram
- Obtenez une instance de la classe Page pour définir le thème
- Attribuez une valeur Preset à la propriété PresetTheme de l'instance Page
- Attribuez une valeur Preset à la propriété PresetThemeVariant de l'instance Page

#### **Appliquer une variante de thème prédéfinie à un exemple de programmation de page**


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


|**Résultat de l'application d'une variante de thème prédéfinie à une page**|
|:- |
|![SetTheme_out.vsdx](theme3.png)|

### **Appliquer un thème prédéfini à une forme**

Les API Aspose.Diagram permettent d'appliquer un thème prédéfini à une forme dans une page. Effectuez les étapes suivantes pour ce faire :

- Créez une instance de la classe Diagram pour charger un diagram
- Obtenez une instance de la classe Shape pour définir le thème
- Attribuez une valeur Preset à la propriété PresetTheme de l'occurrence Shape

#### **Appliquer un thème prédéfini à un exemple de programmation de formes**


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


|**Résultat de l'application d'un thème prédéfini à une forme**|
|:- |
|![SetTheme_out.vsdx](theme4.png)|

### **Appliquer une variante de thème prédéfinie à une forme**

Les API Aspose.Diagram permettent d'appliquer une variante de thème prédéfinie à une forme dans une page. Effectuez les étapes suivantes pour ce faire :

- Créez une instance de la classe Diagram pour charger un diagram
- Obtenez une instance de la classe Shape pour définir le thème
- Attribuez une valeur Preset à la propriété PresetTheme de l'occurrence Shape
- Attribuez une valeur Preset à la propriété PresetThemeVariant de l'occurrence Shape

#### **Appliquer une variante de thème prédéfini à un exemple de programmation de forme**


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


|**Résultat de l'application d'une variante de thème prédéfinie à une forme**|
|:- |
|![SetTheme_out.vsdx](theme5.png)|

### **Appliquer un style rapide de variante de thème prédéfini à une forme**

Aspose.Diagram Les API permettent d'appliquer un style rapide de thème prédéfini à une forme dans une page. Effectuez les étapes suivantes pour ce faire :

- Créez une instance de la classe Diagram pour charger un diagram
- Obtenez une instance de la classe Shape pour définir le thème
- Attribuez une valeur Preset à la propriété PresetTheme de l'occurrence Shape
- Attribuez une valeur Preset à la propriété PresetThemeVariant de l'occurrence Shape
- Attribuez une valeur Preset à la propriété PresetThemeQuickStyle de l'occurrence Shape

#### **Appliquer un style rapide de variante de thème prédéfini à un exemple de programmation de forme**


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


|**Résultat de l'application d'un style rapide de variante de thème prédéfini à une forme**|
|:- |
|![SetTheme_out.vsdx](theme6.png)|

### **Appliquer un style de thème prédéfini à une forme à l'aide de la méthode SetPresetThemeStyleMatrics**

Aspose.Diagram Les API permettent d'appliquer un style rapide de thème prédéfini à une forme dans une page. Effectuez les étapes suivantes pour ce faire :

- Créez une instance de la classe Diagram pour charger un diagram
- Obtenez une instance de la classe Shape pour définir le thème
- Attribuez une valeur Preset à la propriété PresetTheme de l'occurrence Shape
- Attribuez une valeur Preset à la propriété PresetThemeVariant de l'occurrence Shape
- Attribuez un style de thème en définissant la valeur de style et la valeur de couleur de l'instance Shape à l'aide de la méthode setPresetThemeStyleMatrics

#### **Appliquer un style de thème prédéfini à une forme à l'aide de l'exemple de programmation de la méthode setPresetThemeStyleMatrics**


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


|**Résultat de l'application d'un style de thème prédéfini à une forme à l'aide de la méthode setPresetThemeStyleMatrics** |
|:----------------------------------------------------------- |
|![SetTheme_out.vsdx](theme7.png)                             |
