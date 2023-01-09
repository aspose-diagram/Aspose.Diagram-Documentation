---
title: 使用主题
type: docs
weight: 265
url: /zh/java/working-with-themes/
description: 本节介绍如何将预设主题应用到页面或带有 Aspose.Diagram 的形状。
---
## **如何将预设主题应用到页面或形状**
本文对任何想要使用 Aspose.Diagram 修改给定 VSDX 文件主题的人都有用。我们使用测试文件 Themes1.vsdx，如下所示。

|**主题1.vsdx**|
|:- |
|![主题1.vsdx](theme1.png)|

### **将预设主题应用到页面**
Aspose.Diagram API 允许应用预设主题以获得页面内和跨多个文档的形状的统一外观。为此，请执行以下步骤：

- 创建一个Diagram类的实例来加载一个diagram
- 获取要设置主题的Page类实例
- 将 Preset 值分配给 Page 实例的 PresetTheme 属性
#### **将预设主题应用于页面编程示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeForPage.java" >}}

|**将预设主题应用到页面的结果**|
|:- |
|![SetTheme_out.vsdx](theme2.png)|

### **将预设主题变体应用于页面**

Aspose.Diagram API 允许应用预设主题变体以获得页面内和跨多个文档的形状的统一外观。为此，请执行以下步骤：

- 创建一个Diagram类的实例来加载一个diagram
- 获取要设置主题的Page类实例
- 将 Preset 值分配给 Page 实例的 PresetTheme 属性
- 将 Preset 值分配给 Page 实例的 PresetThemeVariant 属性

#### **将预设主题变体应用于页面编程示例**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeVariantForPage.java" >}}

|**将预设主题变体应用于页面的结果**|
|:- |
|![SetTheme_out.vsdx](theme3.png)|

### **将预设主题应用于形状**

Aspose.Diagram API 允许将预设主题应用于页面内的形状。为此，请执行以下步骤：

- 创建一个Diagram类的实例来加载一个diagram
- 获取要设置主题的Shape类实例
- 将 Preset 值分配给 Shape 实例的 PresetTheme 属性

#### **将预设主题应用于形状编程示例**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeForShape.java" >}}

|**将预设主题应用于形状的结果**|
|:- |
|![SetTheme_out.vsdx](theme4.png)|

### **将预设主题变体应用于形状**

Aspose.Diagram API 允许将预设主题变体应用于页面内的形状。为此，请执行以下步骤：

- 创建一个Diagram类的实例来加载一个diagram
- 获取要设置主题的Shape类实例
- 将 Preset 值分配给 Shape 实例的 PresetTheme 属性
- 将预设值分配给 Shape 实例的 PresetThemeVariant 属性

#### **将预设主题变体应用于形状编程示例**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeVariantForShape.java" >}}

|**将预设主题变体应用于形状的结果**|
|:- |
|![SetTheme_out.vsdx](theme5.png)|

### **将预设主题变体快速样式应用于形状**

Aspose.Diagram API 允许将预设主题快速样式应用于页面内的形状。为此，请执行以下步骤：

- 创建一个Diagram类的实例来加载一个diagram
- 获取要设置主题的Shape类实例
- 将 Preset 值分配给 Shape 实例的 PresetTheme 属性
- 将预设值分配给 Shape 实例的 PresetThemeVariant 属性
- 将预设值分配给 Shape 实例的 PresetThemeQuickStyle 属性

#### **将预设主题变体 Quickstyle 应用于形状编程示例**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeQuickStyleForShape.java" >}}

|**将预设主题变体快速样式应用于形状的结果**|
|:- |
|![SetTheme_out.vsdx](theme6.png)|

### **使用 SetPresetThemeStyleMatrics 方法将预设主题样式应用于形状**

Aspose.Diagram API 允许将预设主题快速样式应用于页面内的形状。为此，请执行以下步骤：

- 创建一个Diagram类的实例来加载一个diagram
- 获取要设置主题的Shape类实例
- 将 Preset 值分配给 Shape 实例的 PresetTheme 属性
- 将预设值分配给 Shape 实例的 PresetThemeVariant 属性
- 通过使用 setPresetThemeStyleMatrics 方法设置 Shape 实例的样式值和颜色值来分配主题样式

#### **使用 setPresetThemeStyleMatrics 方法编程示例将预设主题样式应用于形状**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Working-with-Theme-SetThemeStyleMatricsForShape.java" >}}

|**使用 setPresetThemeStyleMatrics 方法将预设主题样式应用于形状的结果** |
|:----------------------------------------------------------- |
|![SetTheme_out.vsdx](theme7.png)                             |
