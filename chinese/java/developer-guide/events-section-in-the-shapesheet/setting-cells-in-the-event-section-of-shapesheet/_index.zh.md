---
title: 在 ShapeSheet 的事件部分中设置单元格
type: docs
weight: 10
url: /zh/java/setting-cells-in-the-event-section-of-shapesheet/
---
{{% alert color="primary" %}} 

使用 Aspose.Diagram API，开发人员可以通过编写自动处理事件的 Visio 公式来定义形状如何响应特定的用户操作。每当用户执行如下所述的操作之一时，就会计算相应 ShapeSheet 单元格中的公式。

- **文本** 当形状的文本或文本组成发生变化时评估的事件元素。
- **事件XFMod** - 形状在页面上的位置、大小或方向已更改。
- **事件DblClick** - 形状被双击。
- **事件掉落** 通过粘贴、复制或拖动形状或拖放母版来创建新实例。
- **事件多点** 当通过粘贴、复制或拖动形状或通过拖放母版创建多个新实例时。
- **数据** 保留供将来使用。

{{% /alert %}} 
## **设置事件单元格**
[事件](https://reference.aspose.com/diagram/java/com.aspose.diagram/event)类允许开发人员在 ShapeSheet 中设置事件单元格。此帮助主题演示了开发人员如何在事件单元格中设置公式：

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-eventsection-SettingEventCells-SettingEventCells.java" >}}
