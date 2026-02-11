---
title: 设置方向并控制隐藏 Visio 保存页面的导出
type: docs
weight: 20
url: /zh/python-java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **将 Visio 页面布局更改为纵向或横向**
Aspose.Diagram for Python via Java API allows developers to set the orientation of the Visio drawing page programmatically. This help topic explains how to accomplish this task.

Aspose.Diagram for Python via Java API has the `Page` class that represents a Visio drawing page. The PageSheet property exposed by the Page class also exposes the print properties. The `PrintPageOrientation` field of the print properties allows to rotate the page. It offers three options as Portrait, Landscape and same as on the printer. The PrintPageOrientation field can be set programmatically using Aspose.Diagram for Python via Java API.

这个例子的工作原理如下：

1. 将现有的 Visio diagram 加载到 Diagram 类对象中。
1. 提取一个Visio页面
1. 将其方向设置为纵向、横向或与打印机相同。
1. 保存 Visio diagram。

### **设置方向编程示例**
下面的代码示例显示了如何设置 Visio 页面的方向。


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# initialize the new visio diagram
diagram = Diagram("DrawingFlowCharts.vsdx")

# get Visio page
page = diagram.getPages().getPage("Flow 1")
# page orientation
page.getPageSheet().getPrintProps().getPrintPageOrientation().setValue(PrintPageOrientationValue.LANDSCAPE)
# save Visio
diagram.save("SetPageOrientation_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}


## **控制导出隐藏的 Visio 页面保存**
Aspose.Diagram for Python via Java API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram for Python via Java API because its option is already available through the cell UIVisibility in the page ShapeSheet.

### **在 Visio Diagram 隐藏一个页面并设置导出选项**
Aspose.Diagram for Python via Java API has the `Page` class that represents a Visio drawing page. The PageSheet property exposed by the Page class also exposes the page properties. The `UIVisibility` field of the page properties allows to hide the page. Developers can then use `exportHiddenPage` property which is added in the `SVGSaveOptions`, `XPSSaveOptions`, `ImageSaveOptions`, `HTMLSaveOptions` and `PdfSaveOptions` classes.

#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")
        
# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)

# initialize PDF save options
options = PdfSaveOptions()
# set export option of hidden Visio pages
options.setExportHiddenPage(False)

# Save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToPDF_Out.pdf", options)

jpype.shutdownJVM()

{{< /highlight >}}


#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)

# initialize PDF save options
options = HTMLSaveOptions()
# set export option of hidden Visio pages
options.setExportHiddenPage(False)
# set export option of comments
options.setExportComments(False)
# Save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToHTML_Out.html", options)

jpype.shutdownJVM()

{{< /highlight >}}


#### **设置图像的导出选项**
下面的代码显示了如何在将 diagram 保存为图像格式之前设置保存选项。


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)
# initialize PDF save options
options = ImageSaveOptions(SaveFileFormat.JPEG)
# set export option of hidden Visio pages
options.setExportHiddenPage(False)
# set export option of comments
options.setExportComments(False)

# Save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToImage_Out.jpeg", options)

jpype.shutdownJVM()

{{< /highlight >}}


#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio
diagram = Diagram("DrawingFlowCharts.vsdx")
# get a particular page
page = diagram.getPages().getPage("Flow 2")
# set Visio page visibility
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE)

# initialize PDF save options
options = SVGSaveOptions()
# set export option of hidden Visio pages
options.setExportHiddenPage(False)
# Set SVG fit to view port
options.setSVGFitToViewPort(True)
# Set export element as Rectangle
options.setExportElementAsRectTag(True)

# save the Visio diagram
diagram.save("ExportOfHiddenVisioPagesToSVG_Out.svg", options)

jpype.shutdownJVM()

{{< /highlight >}}

