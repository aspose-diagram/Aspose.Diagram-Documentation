---
title: 打开文件的不同方式
type: docs
weight: 10
url: /zh/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

使用 Aspose.Diagram 可以轻松打开文件，例如检索数据，或使用设计器模板来加快开发过程。

{{% /alert %}}

## **Opening a File via a Path**

开发人员可以通过在本地计算机上指定文件路径来打开 Microsoft Diagram 文件**Diagram**类构造函数。只需将构造函数中的路径作为*细绳*Aspose.Diagram 会自动检测文件格式类型。


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **Opening a File via a Stream**

将 Visio 文件作为流打开也很简单。为此，请使用构造函数的重载版本，该版本采用*缓冲流*包含文件的对象。


{{< highlight python >}}
import os
import sys
import aspose.diagram
from aspose.diagram import *
from aspose.pyio import BufferStream

#// Build path of an existing diagram
visioDrawing = os.path.join(sourceDir, "Drawing1.vsdx")
# Create a Stream object
f = open(visioDrawing, 'rb')
data = f.read()
databuff = BufferStream(data)
diagram = Diagram(databuff)

#// Save diagram in the VSDX format
diagram.save("Visio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **使用 LoadOptions 打开文件**

要使用加载选项打开文件，请使用**加载选项**classes 为要加载的模板文件设置类的相关选项。


{{< highlight python >}}
import os
import sys
import aspose.diagram
from aspose.diagram import *

#// Build path of an existing diagram
visioDrawing = os.path.join(sourceDir, "Drawing1.vsdx")
# Instantiate LoadOptions specified by the LoadFileFormat
loadOptions = LoadOptions(LoadFileFormat.VSDX)
diagram = Diagram(visioDrawing,loadOptions)

#// Save diagram in the VSDX format
diagram.save("Visio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


