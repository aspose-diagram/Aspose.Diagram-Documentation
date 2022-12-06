---
title: 与大师合作
type: docs
weight: 30
url: /zh/java/working-with-masters/
---
## **检索主信息**
形状母版是 Visio 模板的另一个名称。使用 Aspose.Diagram，可以检索有关页面、连接器和母版的信息。本文介绍如何从 diagram 获取 ID 和名称。

这[掌握](https://reference.aspose.com/diagram/java/com.aspose.diagram/master)对象代表一个[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)对象在 diagram 中的主人。由 Diagram 类公开的 Masters 属性支持 Aspose.Diagram.Master 对象的集合。此属性可用于检索主人的信息，即主人 ID 和名称。

使用 Page.Shapes 属性确定主控形状继承了哪个形状。

**显示代码输出的控制台窗口。** 

![待办事项：图片_替代_文本](http://i.imgur.com/DPn5sP9.png)
### **检索主信息编程示例**
以下代码段从 diagram 中检索主人信息。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-RetrieveMasterInfo-RetrieveMasterInfo.java" >}}
## **从形状模板添加母版**
模板是与特定 Microsoft Office Visio 模板相关联的形状集合。使用 Aspose.Diagram，可以将任何形状母版添加到模板中的绘图中。
### **添加大师**
Master 对象表示 diagram 中 Shape 对象的母版。Diagram 类公开的 AddMaster 方法允许从模板添加母版。它提供了以下四种方式：

- 模板文件路径和主 ID。
- 模板文件路径和主名称。
- 模板文件流和主 ID。
- 模板文件流和主名称。
- 从源 diagram 添加 master 到 diagram
#### **添加主程序示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-AddMasterFromStencil-AddMasterFromStencil.java" >}}
## **从头开始创建大师**
Aspose.Diagram API 允许在没有任何模板、绘图或模板的情况下从头开始创建母版。开发者可以自定义创建Master。 Diagram 类公开的 addMaster 方法允许添加主控。
#### **创建主程序示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CreateMasterfromScratch-CreateMasterfromScratch.java" >}}

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-BASE64Encoder-BASE64Encoder.java" >}}
## **从Visio文件中获取大师**
有时，开发人员需要获得 Visio 图纸的主人的详细信息。 Aspose.Diagram API 支持此功能。

 Aspose.Diagram for Java 提供[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)表示 Visio 绘图的类。 Diagram 类公开的 Masters 属性支持 Aspose.Diagram.Master 对象的集合。此属性可用于检索特定主人的详细信息。 MasterCollection 类公开了 GetMasterByName 和 GetMaster 方法，可以调用这些方法来获取 Master 对象。
### **通过 ID 获取主对象**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Masters 类的 GetMaster 方法。
#### **按 ID 编程示例的主对象**
以下示例显示如何通过 ID 从 Visio 绘图中获取母版。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-GetMasterbyID-GetMasterbyID.java" >}}
### **按名称获取主对象**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Masters 类的 GetMasterByName 方法。
#### **按名称编程示例的主对象**
以下示例显示如何从 Visio 绘图中按名称获取主对象。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-GetMasterbyName-GetMasterbyName.java" >}}
## **检查 Visio 绘图中是否存在大师**
Aspose.Diagram API 支持检查 Visio 绘图中是否存在母版。使用 MasterCollection 属性，开发人员可以通过名称或 ID 检查母版是否存在。

 Aspose.Diagram for Java 提供[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)表示 Visio 绘图的类。 Diagram 类公开的 Masters 属性支持 Aspose.Diagram.Master 对象的集合。此属性可用于检查特定主机的存在。 MasterCollection 类公开了可以使用主名称或 ID 参数调用的 IsExist 方法。
### **通过 ID 检查主状态**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Masters 类的 IsExist 方法。
#### **Master Presence by ID 编程示例**
以下示例显示如何在 Visio 图形中按 ID 检查主控图是否存在。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CheckMasterPresencebyID-CheckMasterPresencebyID.java" >}}
### **按名称检查主状态**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Masters 类的 IsExist 方法。
#### **Master Presence by Name 编程示例**
以下示例显示如何按名称检查 Visio 图形中的主控存在。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CheckMasterPresencebyName-CheckMasterPresencebyName.java" >}}
