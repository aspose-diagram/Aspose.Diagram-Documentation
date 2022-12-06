---
title: 配置渲染字体
type: docs
weight: 10
url: /zh/net/configuring-fonts-for-rendering/
---
## **可能的使用场景**

Aspose.Diagram API 提供了以图像格式呈现页面以及将它们转换为 PDF 和 XPS 格式的工具。为了最大限度地提高转换保真度，电子表格中使用的字体必须在操作系统的默认字体目录中可用。如果所需字体不存在，则 Aspose.Diagram API 将尝试用可用字体替换所需字体。

## **字体选择**

以下是 Aspose.Diagram API 在幕后遵循的过程。

1. API 尝试在文件系统上查找与电子表格中使用的确切字体名称匹配的字体。
1. 如果API找不到下定义的字体**[SaveOptions.DefaultFont](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/defaultfont/)**属性，它会尝试使用下面指定的字体**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)**财产。
1. 如果API找不到下定义的字体**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)**属性，它会尝试从所有可用字体中选择最合适的字体。
1. 最后，如果 API 在文件系统上找不到任何字体，它会使用 Times New Roman 呈现页面。

## **设置自定义字体文件夹**

Aspose.Diagram API 在操作系统的默认字体目录中搜索所需的字体。如果所需的字体在系统的字体目录中不可用，则 API 会搜索自定义（用户定义的）目录。这**[字体配置](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/)**类公开了许多设置自定义字体目录的方法，如下所述。

1. **[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)**：如果只设置一个文件夹，此方法很有用。

1. **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)**：当字体位于多个文件夹中并且用户希望单独设置所有文件夹而不是将所有字体组合在一个文件夹中时，此方法很有用。
1. **[FontConfigs.SetFontSources](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontsources/)**：当用户希望从多个文件夹或单个字体文件或字节数组中加载字体数据时，此机制很有用。

{{% alert color="primary" %}}

两个都**[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)** & **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)**方法接受布尔类型的第二个参数。通过**真的**因为第二个参数将指示 Aspose.Diagram API 在子文件夹中搜索字体文件。

{{% /alert %}}

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-OS-Fonts-Location-SetCustomFontFolders-SetCustomFontFolders.cs" >}}

{{% alert color="primary" %}}

请在申请开始时使用上述任何一种方法，即；在调用 Aspose.Diagram API 的任何其他对象之前。

{{% /alert %}} {{% alert color="primary" %}}

如果上述所有方法都用于设置字体源，则只有最后的设置生效。

{{% /alert %}}

