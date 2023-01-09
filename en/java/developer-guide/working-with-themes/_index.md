---
title: Working with Themes
type: docs
weight: 265
url: /java/working-with-themes/
description: This section explains how to apply a preset theme to a page or a shape with Aspose.Diagram.
---

## **How to Apply a Preset theme to a Page or a Shape**
This article can be useful to anyone who wants to modify the theme of a giving VSDX file using Aspose.Diagram. We use a test file Themes1.vsdx, look like below.

|**Theme1.vsdx**|
| :- |
|![Theme1.vsdx](theme1.png)|

### **Apply a Preset Theme to a Page**
Aspose.Diagram APIs allows to apply a preset theme to get a uniform look and feel to shapes within a page, and across multiple documents. Perform the following steps in order to do this:

- Create an instance of Diagram class to load a diagram
- Get an instance of Page class to be set theme
- Assign a Preset value to the PresetTheme property of the Page instance
#### **Apply a Preset Theme to a Page Programming Sample**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeForPage.java" >}}

|**Result of Apply a Preset Theme to a Page**|
| :- |
|![SetTheme_out.vsdx](theme2.png)|

### **Apply a Preset Theme Variant to a Page**

Aspose.Diagram APIs allows to apply a preset theme variant to get a uniform look and feel to shapes within a page, and across multiple documents. Perform the following steps in order to do this:

- Create an instance of Diagram class to load a diagram
- Get an instance of Page class to be set theme
- Assign a Preset value to the PresetTheme property of the Page instance
- Assign a Preset value to the PresetThemeVariant property of the Page instance

#### **Apply a Preset Theme Variant to a Page Programming Sample**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeVariantForPage.java" >}}

|**Result of Apply a Preset Theme Variant to a Page**|
| :- |
|![SetTheme_out.vsdx](theme3.png)|

### **Apply a Preset Theme to a Shape**

Aspose.Diagram APIs allows to apply a preset theme to a shape within a page. Perform the following steps in order to do this:

- Create an instance of Diagram class to load a diagram
- Get an instance of Shape class to be set theme
- Assign a Preset value to the PresetTheme property of the Shape instance

#### **Apply a Preset Theme to a Shape Programming Sample**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeForShape.java" >}}

|**Result of Apply a Preset Theme to a Shape**|
| :- |
|![SetTheme_out.vsdx](theme4.png)|

### **Apply a Preset Theme Variant to a Shape**

Aspose.Diagram APIs allows to apply a preset theme variant to a shape within a page. Perform the following steps in order to do this:

- Create an instance of Diagram class to load a diagram
- Get an instance of Shape class to be set theme
- Assign a Preset value to the PresetTheme property of the Shape instance
- Assign a Preset value to the PresetThemeVariant property of the Shape instance

#### **Apply a Preset Theme Variant to a Shape Programming Sample**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeVariantForShape.java" >}}

|**Result of Apply a Preset Theme Variant to a Shape**|
| :- |
|![SetTheme_out.vsdx](theme5.png)|

### **Apply a Preset Theme Variant Quickstyle to a Shape**

Aspose.Diagram APIs allows to apply a preset theme quickstyle to a shape within a page. Perform the following steps in order to do this:

- Create an instance of Diagram class to load a diagram
- Get an instance of Shape class to be set theme
- Assign a Preset value to the PresetTheme property of the Shape instance
- Assign a Preset value to the PresetThemeVariant property of the Shape instance
- Assign a Preset value to the PresetThemeQuickStyle property of the Shape instance

#### **Apply a Preset Theme Variant Quickstyle to a Shape Programming Sample**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeQuickStyleForShape.java" >}}

|**Result of Apply a Preset Theme Variant Quickstyle to a Shape**|
| :- |
|![SetTheme_out.vsdx](theme6.png)|

### **Apply a Preset Theme Style to a Shape Using SetPresetThemeStyleMatrics Method**

Aspose.Diagram APIs allows to apply a preset theme quickstyle to a shape within a page. Perform the following steps in order to do this:

- Create an instance of Diagram class to load a diagram
- Get an instance of Shape class to be set theme
- Assign a Preset value to the PresetTheme property of the Shape instance
- Assign a Preset value to the PresetThemeVariant property of the Shape instance
- Assign a theme style by setting style value and color value of the Shape instance using setPresetThemeStyleMatrics Method

#### **Apply a Preset Theme Style to a Shape Using setPresetThemeStyleMatrics Method Programming Sample**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeStyleMatricsForShape.java" >}}

| **Result of Apply a Preset Theme Style to a Shape Using setPresetThemeStyleMatrics Method** |
| :----------------------------------------------------------- |
| ![SetTheme_out.vsdx](theme7.png)                             |
