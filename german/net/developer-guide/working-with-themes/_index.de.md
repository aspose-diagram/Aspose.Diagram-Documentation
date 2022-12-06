---
title: Arbeiten mit Themen
type: docs
weight: 265
url: /de/net/working-with-themes/
description: In diesem Abschnitt wird erläutert, wie Sie mit Aspose.Diagram ein voreingestelltes Design auf eine Seite oder eine Form anwenden.
---
## **So wenden Sie ein voreingestelltes Design auf eine Seite oder eine Form an**
Dieser Artikel kann für jeden nützlich sein, der das Thema einer gebenden VSDX-Datei mit Aspose.Diagram ändern möchte. Wir verwenden eine Testdatei Themes1.vsdx, die wie unten aussieht.

|**Thema1.vsdx**|
|:- |
|![Thema1.vsdx](theme1.png)|

### **Wenden Sie ein voreingestelltes Design auf eine Seite an**
Aspose.Diagram APIs ermöglichen die Anwendung eines voreingestellten Designs, um ein einheitliches Erscheinungsbild für Formen auf einer Seite und über mehrere Dokumente hinweg zu erhalten. Führen Sie dazu die folgenden Schritte aus:

- Erstellen Sie eine Instanz der Klasse Diagram, um eine diagram zu laden
- Holen Sie sich eine Instanz der Page-Klasse, um das Thema festzulegen
- Weisen Sie der PresetTheme-Eigenschaft der Page-Instanz einen Preset-Wert zu
#### **Wenden Sie ein voreingestelltes Design auf ein Beispiel für die Seitenprogrammierung an**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeForPage.cs" >}}

|**Ergebnis der Anwendung eines voreingestellten Designs auf eine Seite**|
|:- |
|![SetTheme_out.vsdx](theme2.png)|

### **Wenden Sie eine voreingestellte Designvariante auf eine Seite an**

Aspose.Diagram-APIs ermöglichen das Anwenden einer voreingestellten Designvariante, um ein einheitliches Erscheinungsbild für Formen auf einer Seite und über mehrere Dokumente hinweg zu erhalten. Führen Sie dazu die folgenden Schritte aus:

- Erstellen Sie eine Instanz der Klasse Diagram, um eine diagram zu laden
- Holen Sie sich eine Instanz der Page-Klasse, um das Thema festzulegen
- Weisen Sie der PresetTheme-Eigenschaft der Page-Instanz einen Preset-Wert zu
- Weisen Sie der PresetThemeVariant-Eigenschaft der Page-Instanz einen Preset-Wert zu

#### **Wenden Sie eine voreingestellte Designvariante auf ein Beispiel für die Seitenprogrammierung an**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeVariantForPage.cs" >}}

|**Ergebnis der Anwendung einer voreingestellten Designvariante auf eine Seite**|
|:- |
|![SetTheme_out.vsdx](theme3.png)|

### **Wenden Sie ein voreingestelltes Design auf eine Form an**

Aspose.Diagram APIs ermöglichen das Anwenden eines voreingestellten Designs auf eine Form innerhalb einer Seite. Führen Sie dazu die folgenden Schritte aus:

- Erstellen Sie eine Instanz der Klasse Diagram, um eine diagram zu laden
- Holen Sie sich eine Instanz der Shape-Klasse, um das Thema festzulegen
- Weisen Sie der PresetTheme-Eigenschaft der Shape-Instanz einen Preset-Wert zu

#### **Wenden Sie ein voreingestelltes Design auf ein Shape-Programmierbeispiel an**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeForShape.cs" >}}

|**Ergebnis der Anwendung eines voreingestellten Designs auf eine Form**|
|:- |
|![SetTheme_out.vsdx](theme4.png)|

### **Wenden Sie eine voreingestellte Designvariante auf eine Form an**

Aspose.Diagram APIs ermöglichen das Anwenden einer voreingestellten Designvariante auf eine Form innerhalb einer Seite. Führen Sie dazu die folgenden Schritte aus:

- Erstellen Sie eine Instanz der Klasse Diagram, um eine diagram zu laden
- Holen Sie sich eine Instanz der Shape-Klasse, um das Thema festzulegen
- Weisen Sie der PresetTheme-Eigenschaft der Shape-Instanz einen Preset-Wert zu
- Weisen Sie der PresetThemeVariant-Eigenschaft der Shape-Instanz einen Preset-Wert zu

#### **Wenden Sie eine voreingestellte Designvariante auf ein Shape-Programmierbeispiel an**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeVariantForShape.cs" >}}

|**Ergebnis der Anwendung einer voreingestellten Designvariante auf eine Form**|
|:- |
|![SetTheme_out.vsdx](theme5.png)|

### **Wenden Sie einen Quickstyle einer voreingestellten Designvariante auf eine Form an**

Aspose.Diagram APIs ermöglichen das Anwenden eines voreingestellten Design-Schnellstils auf eine Form innerhalb einer Seite. Führen Sie dazu die folgenden Schritte aus:

- Erstellen Sie eine Instanz der Klasse Diagram, um eine diagram zu laden
- Holen Sie sich eine Instanz der Shape-Klasse, um das Thema festzulegen
- Weisen Sie der PresetTheme-Eigenschaft der Shape-Instanz einen Preset-Wert zu
- Weisen Sie der PresetThemeVariant-Eigenschaft der Shape-Instanz einen Preset-Wert zu
- Weisen Sie der PresetThemeQuickStyle-Eigenschaft der Shape-Instanz einen Preset-Wert zu

#### **Wenden Sie eine voreingestellte Themenvariante Quickstyle auf ein Shape-Programmierbeispiel an**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeQuickStyleForShape.cs" >}}

|**Ergebnis des Anwendens einer voreingestellten Designvariante Quickstyle auf eine Form**|
|:- |
|![SetTheme_out.vsdx](theme6.png)|

### **Wenden Sie mithilfe der SetPresetThemeStyleMatrics-Methode einen voreingestellten Designstil auf eine Form an**

Aspose.Diagram APIs ermöglichen das Anwenden eines voreingestellten Design-Schnellstils auf eine Form innerhalb einer Seite. Führen Sie dazu die folgenden Schritte aus:

- Erstellen Sie eine Instanz der Klasse Diagram, um eine diagram zu laden
- Holen Sie sich eine Instanz der Shape-Klasse, um das Thema festzulegen
- Weisen Sie der PresetTheme-Eigenschaft der Shape-Instanz einen Preset-Wert zu
- Weisen Sie der PresetThemeVariant-Eigenschaft der Shape-Instanz einen Preset-Wert zu
- Weisen Sie einen Designstil zu, indem Sie den Stilwert und den Farbwert der Shape-Instanz mithilfe der SetPresetThemeStyleMatrics-Methode festlegen

#### **Anwenden eines voreingestellten Designstils auf eine Form mithilfe des Programmierungsbeispiels für die SetPresetThemeStyleMatrics-Methode**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeStyleMatricsForShape.cs" >}}

|**Ergebnis des Anwendens eines voreingestellten Designstils auf eine Form mithilfe der SetPresetThemeStyleMatrics-Methode**|
|:- |
|![SetTheme_out.vsdx](theme7.png)|
