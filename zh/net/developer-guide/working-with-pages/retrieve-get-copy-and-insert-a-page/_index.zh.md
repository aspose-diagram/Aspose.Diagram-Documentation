---
title: 检索、获取、复制和插入页面
type: docs
weight: 10
url: /zh/net/retrieve-get-copy-and-insert-a-page/
description: 本节介绍如何使用 Aspose.Diagram 插入页面、复制页面或获取页面信息。
---
## **检索页面信息**
在 Microsoft Visio 中，页面要么是前景页面，要么是背景页面。要获取页面信息，例如页面 ID 和页面名称，首先要确定页面是背景页面还是前景页面。

这[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)对象表示前景页面或背景页面的绘图区域。公开的 Pages 属性[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类支持 Aspose.Diagram.Page 对象的集合。此属性可用于检索页面信息。

使用 Page.Background 属性确定页面是前景页面还是背景页面。
### **检索页面信息编程示例**
以下代码从 diagram 中检索页面信息。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-RetrievePageInfo-RetrievePageInfo.cs" >}}
## **从 Diagram 获取 Visio 页面**
有时，开发人员需要获取 Visio 图的页面详细信息。 Aspose.Diagram 具有帮助他们做到这一点的功能。

 Aspose.Diagram for .NET 提供[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)表示 Visio 绘图的类。 Diagram 类公开的 Pages 属性支持 Aspose.Diagram.Page 对象的集合。 PageCollection 类公开了可以调用以获取 Page 对象的 GetPage 方法。
### **通过 ID 获取 Visio 页面对象**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Pages 类的 GetPage 方法。

以下示例显示如何通过 id 从 Visio 绘图中获取页面对象。
#### **通过 ID 获取页面对象编程示例**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-GetVisioPagebyID-GetVisioPagebyID.cs" >}}
### **按名称获取 Visio 页面对象**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Pages 类的 GetPage 方法。
#### **按名称获取页面对象编程示例**
以下示例显示如何从 Visio 绘图中按名称获取页面对象。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-GetVisioPagebyName-GetVisioPagebyName.cs" >}}
## **将 Visio 页面复制到另一个 Diagram**
Aspose.Diagram for .NET API 允许开发人员将其内容从一个 Visio diagram 复制并添加到另一个。此帮助主题说明了如何完成此任务。

 Aspose.Diagram for .NET API 有[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)表示 Visio 绘图的类。 Diagram 类公开的 Pages 属性支持 Aspose.Diagram.Page 对象的集合。 PageCollection 类公开了可以调用以添加另一个 Page 对象的 Add 方法。

这个例子的工作原理如下：

1. 创建 Diagram 类的新对象。
1. 将现有的 Visio diagram 加载到 Diagram 类对象中。
1. 添加加载的所有母版 Visio diagram
1. 从加载的 diagram（需要复制）中获取页面对象。
1. 设置页面对象名称和 ID。
1. 删除新的 diagram（可选）的空白页。
1. 调用 PageCollection 类的 Add 方法。
1. 将新的 diagram 保存在计算机存储中。
### **复制一个Visio页面编程样例**
下面的代码示例显示了如何将 Visio 页面对象复制到另一个 Visio 绘图中。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-CopyVisioPage-CopyVisioPage.cs" >}}
## **将 Visio Page 复制到另一个 Page 实例**
Page 类的 Copy 方法采用要克隆的页面实例。

**C#**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.Copy(diagram.Pages.GetPage("Page-1"));

{{< /highlight >}}
## **在 Visio 绘图中插入空白页**
[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx)可以在 Microsoft Office Visio 绘图中插入一个新的空白页。本示例主题描述了如何执行此操作。

Pages 集合公开的 Add 方法允许开发人员在 Visio diagram 中添加一个新的空白页面。应该分配页面 ID。
### **插入空白页编程示例**
下面的一段代码在 Visio 绘图中插入了一个空白页：

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-InsertBlankPageInVisio-InsertBlankPageInVisio.cs" >}}
## **在 Visio 绘图中移动页面位置**
Aspose.Diagram for .NET API 可以在Visio绘图中移动页面位置。 Page 类公开的 MoveTo 方法可帮助开发人员移动页面位置。
### **移动页面位置编程示例**
MoveTo成员以目标页面索引为参数，移动页面在Visio图中的位置：

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

diagram.Save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
