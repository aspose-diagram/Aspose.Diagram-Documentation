---
title: Connect Shapes
type: docs
weight: 90
url: /python-java/connect-shapes/
description: This section explains how to connect two shapes with Aspose.Diagram for Python via Java.
---

## **Connect Shapes**
This section explains how to connect two shapes using Aspose.Diagram for Python via Java.
### **Connect Shapes**
The [connectShapesViaConnector](https://reference.aspose.com/diagram/python-java/asposediagram.api/page#connectShapesViaConnector(long,%20java.lang.String,%20long,%20java.lang.String,%20long)) method connect two shapes via a connector in the [Page](https://reference.aspose.com/diagram/python-java/asposediagram.api/Page) class.

The code below shows how to:

1. Create a diagram from stencil.
1. Add two shapes to page.
1. Add a connector shape to page.
1. Connect the two shapes with the connector using connectShapesViaConnector mothod
1. save diagram
#### **Connect Shapes Programming Sample**
Use the following code to connect shapes using Aspose.Diagram for Java.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load diagram
diagram = Diagram()

# Load stencil to a stream
templateFileName = "NetApp-FAS-series.vss"

# Add master with stencil file path and master id
diagram.addMaster(templateFileName, 2)

# Add master with stencil file path and master name
masterName = "FAS80xx rear empty"
diagram.addMaster(templateFileName, masterName)

# adds master to diagram from source diagram
src = Diagram(templateFileName)
diagram.addMaster(src, masterName)

# Adds shape with defined PinX and PinY.
diagram.addShape(2.0, 2.0, masterName, 0)
diagram.addShape(6.0, 6.0, masterName, 0)

diagram.save("AddMasterFromStencil_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```

|**Result**|
| :- |
|![ConnectShapes_out.vsdx](ConnectShapes.png)|