---
title: 将主题应用于形状
type: docs
weight: 70
url: /zh/net/apply-theme-to-shape/
description: 本节介绍如何使用 Aspose.Diagram 在 visio 形状中设置主题属性。
---
## **在 Visio 中将主题颜色设置为形状**
本主题详细说明开发人员如何使用 Aspose.Diagram for .NET 将主题颜色应用于形状。

下面的代码显示了如何：

1. 加载示例 diagram。
1. 获取特定页面。
1. 得到一个特定的形状。
1. 设置形状的主题。
1. 保存 diagram
#### **将主题设置为形状编程示例**
在您的 .NET 应用程序中使用以下代码，使用 Aspose.Diagram for .NET 设置连接器类型形状的外观。


{{< highlight csharp >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-2");

// Add master with stencil file path and master name
string masterName = "Rectangle";
diagram.AddMaster(dataDir + "Basic Shapes.vss", masterName);

// Page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
// Add a new rectangle shape
long rectangleId = diagram.AddShape(pinX, pinY, width, height, masterName, PageIndex);

// Set shape properties 
Shape rectangle = page.Shapes.GetShape(rectangleId);
rectangle.XForm.PinX.Value = 5;
rectangle.XForm.PinY.Value = 5;
rectangle.Type = TypeValue.Shape;
rectangle.Text.Value.Add(new Txt("Aspose Diagram"));

// Apply preset theme clouds to new shape in page "Page-2"
rectangle.PresetTheme = PresetThemeValue.Clouds;
rectangle.PresetThemeVariant = PresetThemeVariantValue.Variant1;
rectangle.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle1;

// Apply preset theme bubble to page "Page-3"
Page page3 = diagram.Pages.GetPage("Page-3");
page3.PresetTheme = PresetThemeValue.Bubble;
page3.PresetThemeVariant = PresetThemeVariantValue.Variant2;
page3.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle3;

diagram.Save(dataDir + "ApplyThemeToNewShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

