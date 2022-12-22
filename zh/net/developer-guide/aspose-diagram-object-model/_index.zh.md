---
title: Aspose.Diagram 对象模型
linktitle: Aspose.Diagram 对象模型
type: docs
description: Aspose.Diagram 对象模型提供有关 Aspose.Diagram 类库对象之间结构关系的信息。
weight: 20
url: /zh/net/object_model
---
{{% alert color="primary" %}} 

**Aspose.Diagram 对象模型**

Aspose.Diagram 对象模型提供有关 Aspose.Diagram 类库对象之间结构关系的信息。

{{% /alert %}} 

### Aspose.Diagram 对象模型的顶层结构如下图所示。

|**Aspose.Diagram对象模型的顶层结构**|
|:- |
|![Aspose.Diagram对象模型的顶层结构](diagram-classes.png)|

从上图可以看出，对象模型的根是Diagram对象。为了介绍的目的，下面提供了一些对象的简要描述。

#### **页面集合/页面**

Diagram对象包含了PageCollection，它代表了一个Diagram中所有Page对象的集合。

#### **形状集合/形状**

Page 对象包含 ShapeCollection，它表示 Page 中所有 Shape 对象的集合。 Shape 对象包含在 Master、Page 或 group shape 元素中定义形状的元素。

#### **ConnectCollection/连接**

Page 对象包含 ConnectCollection，它表示 Page 中所有 Connect 对象的集合。 Connect 对象表示绘图中两个形状之间的连接，例如组织结构图中的一条线和一个框。

#### **样式表集合/样式表**

表示文档中定义的样式。

#### **MasterCollection/硕士**

包含定义文档母版的元素。母版是模板上的形状，您可以重复使用它来创建绘图。当您将形状从模板拖到绘图页上时，该形状成为该母版的实例，母版的本地副本包含在文档中。

#### **文档属性**

包含文档属性元素，例如文档的标题、作者等。

#### **页眉页脚**

包含文档页眉和页脚的元素。

#### **Vba项目**

表示 VBA 项目。

#### **ThemeCollection/主题**

动态主题定义属性，这些属性指定颜色、字体、填充、线条属性和效果的属性。

#### **充满**

包含形状和形状的投影的当前填充格式值，包括图案、前景色和背景色。

#### **线**

包含控制形状线条属性的元素，例如图案、粗细和颜色。这些元素决定线端是否格式化（例如，带箭头）、线端格式的大小、应用于线的圆角圆的半径以及线端样式（圆形或方形）。

#### **几何学**

包含一组 Geom 元素。

#### **字符**

包含 Char 对象的集合，其中包含形状的文本样式。

#### **文本**

包含形状的文本。

#### **变形**

包含指定有关形状的一般定位信息的元素。

#### **文本XForm**

包含指定有关形状文本块的定位信息的元素。

#### **HyperlinkCollection/超链接**

超链接对象包含用于在形状或绘图页与另一个绘图页、另一个文件或网站之间创建多个跳转的元素。

#### **大师造型**

此属性可能仅出现在作为组形状成员的形状中，并且该组是母版的实例。该属性包含一个引用母版中相应子形状的 ID。

#### **FieldCollection/字段**

字段对象包含指定插入到形状文本中的函数和公式的元素。
