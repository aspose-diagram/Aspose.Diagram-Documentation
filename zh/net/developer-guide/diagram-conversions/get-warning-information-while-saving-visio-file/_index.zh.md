---
title: 保存 Visio 文件时获取警告信息
type: docs
weight: 110
url: /zh/net/get-warning-information-while-saving-visio-file/
---
## **可能的使用场景**

有时用户会尝试保存包含没有本地字体的文本的 diagram。在这种情况下，Aspose.Diagram 在保存 diagram 时抛出警告。您可以通过实施**[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)**界面与设置**[SaveOptions.WarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)**财产。

## **保存 Visio 文件时收到警告**

以下示例代码说明了如何在保存 visio 文件时收到警告。代码转换[样本 visio 文件](sampleFontSubstitution.vsdx)哪个抛出**[字体替换](https://reference.aspose.com/diagram/net/aspose.diagram/warningtype)**保存警告。这个警告然后被捕获**[IWarningCallback.Warning()](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)**在控制台上打印警告消息的方法。另请检查下面给出的代码的控制台输出以获得更多理解。

## **示例代码**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-GetWarningInformation.cs" >}}

## **控制台输出**

这是使用提供的执行时上述代码的控制台输出[样本 visio 文件](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
