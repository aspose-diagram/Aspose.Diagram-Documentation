---
title: 检索、获取、复制和插入页面
type: docs
weight: 10
url: /zh/python-java/retrieve-get-copy-and-insert-a-page/
---
## **检索页面信息**
在 Microsoft Visio 中，页面要么是前景页面，要么是背景页面。要获取页面信息，例如页面 ID 和页面名称，首先要确定页面是背景页面还是前景页面。

`Page` 对象表示前景页面或背景页面的绘图区域。 `Diagram` 类公开的 Pages 属性支持 Pages 对象的集合。此属性可用于检索页面信息。

使用 `Page.Background` 属性确定页面是前景页面还是背景页面。

### **检索页面信息编程示例**
以下代码从 diagram 中检索页面信息。

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram
diagram = Diagram("RetrievePageInfo.vdx")

for page in diagram.getPages():
    # Checks if current page is a background page
    if page.getBackground() == BOOL.TRUE:
        # Display information about the background page
        print("Background Page ID : " + str(page.getID()))
        print("Background Page Name : " + str(page.getName()))
    else:
        # Display information about the foreground page
        print("\nPage ID : " + str(page.getID()))
        print("Universal Name : " + str(page.getNameU()))
        print("ID of the Background Page : " + str(page.getBackPage()))

jpype.shutdownJVM()

{{< /highlight >}}
```

## **从 Diagram 获取 Visio 页面**
Sometimes, developers need to get a Visio drawing's page details. Aspose.Diagram for Python via Java has features that helps them do this.

Aspose.Diagram for Python via Java offers the `Diagram` class that represents a Visio drawing. The Pages property exposed by the Diagram class supports a collection of `Page` objects. The PageCollection class exposes `getPage` method that can be called to get Page object.

### **通过 ID 获取 Visio 页面对象**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Pages 类的 getPage 方法。

以下示例显示如何通过 id 从 Visio 绘图中获取页面对象。

#### **通过 ID 获取页面对象编程示例**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VDX file
diagram = Diagram("DrawingFlowCharts.vsdx")

# Set page id
page_id = 2
# Get page object by id
page2 = diagram.getPages().getPage(page_id)

jpype.shutdownJVM()

{{< /highlight >}}
```

### **按名称获取 Visio 页面对象**
这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 调用 Diagram.Pages 类的 GetPage 方法。

#### **按名称获取页面对象编程示例**
以下示例显示如何从 Visio 绘图中按名称获取页面对象。

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSDX file
diagram = Diagram("DrawingFlowCharts.vsdx")

# Set page name
pageName = "Flow 2"
# Get page object by name
page2 = diagram.getPages().getPage(pageName)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **将 Visio 页面复制到另一个 Diagram**
Aspose.Diagram for Python via Java API allows developers to copy and add its content from the one Visio diagram to another. This help topic explains how to accomplish this task.

Aspose.Diagram for Python via Java API has the `Diagram` class that represents a Visio drawing. The Pages property exposed by the Diagram class supports a collection of `Page` objects. The PageCollection class exposes `add` method that can be called to add another Page object.

这个例子的工作原理如下：

1. 创建 Diagram 类的新对象。
1. 将现有的 Visio diagram 加载到 Diagram 类对象中。
1. 添加加载的所有母版 Visio diagram
1. 从加载的 diagram（需要复制）中获取页面对象。
1. 设置页面对象名称和 ID。
1. 删除新的 diagram（可选）的空白页。
1. 调用 PageCollection 类的 add 方法。
1. 将新的 diagram 保存在计算机存储中。

### **复制一个Visio页面编程样例**
下面的代码示例显示了如何将 Visio 页面对象复制到另一个 Visio 绘图中。

```
{{< highlight "python" >}}
import jpype
import asposediagram

jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
originalDiagram = Diagram("Drawing1.vsdx")

# initialize the new visio diagram
newDiagram = Diagram()

# add all masters from the source Visio diagram
originalMasters = originalDiagram.getMasters()
for master in originalMasters:
    newDiagram.addMaster(originalDiagram, master.getName())

# get the page object from the original diagram
SrcPage = originalDiagram.getPages().getPage("Page-1")
# set page name
SrcPage.setName("new page")

# it calculates max page id
max_page_id = 0
if newDiagram.getPages().getCount() != 0:
    max_page_id = newDiagram.getPages().get(0).getID()

for i in range(0, newDiagram.getPages().getCount() - 1):
    if max_page_id < newDiagram.getPages().get(i).getID():
        max_page_id = newDiagram.getPages().get(i).getID()

MaxPageId = max_page_id
# set page id
SrcPage.setID(MaxPageId)
# add reference of the original diagram page
newDiagram.getPages().add(SrcPage)

# remove first empty page
newDiagram.getPages().remove(newDiagram.getPages().get(0))

# save diagram in VDX format
newDiagram.save("CopyVisioPage_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **将 Visio Page 复制到另一个 Page 实例**
`Page` 类的 `copy` 方法需要一个页面实例来克隆。

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page()

# copy page

newPage.copy(diagram.getPages().getPage("Page-1"))

```

## **在 Visio 绘图中插入空白页**
Aspose.Diagram for Python via Java can insert a new blank page into the Microsoft Office Visio drawing. This example topic describes how to do so.

`add` 方法，由 Pages 集合公开，允许开发者在 Visio diagram 中添加一个新的空白页面。页面 ID 应该被分配。

### **插入空白页编程示例**
下面的一段代码在 Visio 绘图中插入了一个空白页：

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("Drawing1.vsdx")
        
# it calculates max page id
max_page_id = 0
if diagram.getPages().getCount() != 0:
    max_page_id = diagram.getPages().get(0).getID()

for i in range(0, diagram.getPages().getCount() - 1):
    if max_page_id < diagram.getPages().get(i).getID():
        max_page_id = diagram.getPages().get(i).getID()
        
# Initialize a new page object
newPage = Page()
# Set name
newPage.setName("new page")
# Set page ID
newPage.setID(max_page_id + 1)

# Or try the Page constructor
# Page newPage = Page(MaxPageId + 1)

# Add a new blank page
diagram.getPages().add(newPage)

# Save diagram
diagram.save("InsertBlankPageInVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **在 Visio 绘图中移动页面位置**
Aspose.Diagram for Python via Java API can move page position in the Visio drawing. The `moveTo` method, exposed by the `Page` class, helps developers to move the page position.

### **移动页面位置编程示例**
MoveTo成员以目标页面索引为参数，移动页面在Visio图中的位置：

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page(1)

# move page in the diagram

newPage.moveTo(2)

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX)
```
