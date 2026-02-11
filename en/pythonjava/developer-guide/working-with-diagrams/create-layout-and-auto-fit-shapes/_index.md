---
title: Create, Layout and Auto-Fit Shapes
type: docs
weight: 10
url: /python-java/create-layout-and-auto-fit-shapes/
---

## **Creating a Diagram**
Aspose.Diagram for Python via Java lets you read and create Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. The first step when creating new documents, is to create a diagram. Then [add shapes and connectors](/diagram/python-java/add-and-connect-visio-shapes/) to build up the diagram. Use the default constructor of Diagram class to create a new diagram.
### **Programming Sample**
```
{{< highlight "python" >}}
import jpype
import os
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# initialize a new Diagram
diagram = Diagram()
# save in the VSDX format
diagram.save("CreateDiagram_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
## **Layout Shapes in Flowchart Style**
With certain types of connected drawings, such as flowcharts and network diagrams, you can use the **Layout Shapes** feature to automatically position shapes. Automatically positioning is faster than manually dragging each shape to a new location.

For example, if you're updating a large flowchart to include a new process, you can add and connect the shapes that make up the process, and then use the layout feature to automatically layout the updated drawing.

The Layout method, exposed by the Diagram class layouts the shapes and/or reroutes the connectors on all the diagram's pages. This method accepts an LayoutOptions object as an argument. Use the different properties exposed by the LayoutOptions class to automatically layout shapes.

The image below shows the diagram loaded by the code snippets in this article, before auto layout is applied. The code snippets show how to apply flowchart layouts and compact tree layouts.

**The source diagram.** 

![todo:image_alt_text](create-layout-and-auto-fit-shapes_1.png)

The code snippets in this article takes the source diagram and applies several types of auto layout to it, saving each in a separate file.

|<p>**Layout shapes bottom to top** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**Layout shapes top to bottom** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_3.png)</p>|
| :- | :- |
|<p>**Layout shapes left to right** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**Layout shapes right to left** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_5.png)</p>|
To layout shapes in flowchart style:

1. Create an instance of the Diagram class.
1. Create an instance of LayoutOptions class and set Flowchart style related properties.
1. Call the Diagram class' Layout method by passing LayoutOptions.
1. Call the Diagram class' Save method to write the Visio drawing.
### **Flowchart Style Programming Sample**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load an existing Visio diagram
fileName = "LayOutShapesInFlowchartStyle.vdx"
diagram = Diagram(fileName)

# set layout options
flowChartOptions = LayoutOptions()
flowChartOptions.setLayoutStyle(LayoutStyle.FLOW_CHART)
flowChartOptions.setSpaceShapes(1)
flowChartOptions.setEnlargePage(True)

# set layout direction as BottomToTop and then save
flowChartOptions.setDirection(LayoutDirection.BOTTOM_TO_TOP)
diagram.layout(flowChartOptions)
diagram.save("sample_btm_top.vdx", SaveFileFormat.VDX)

# set layout direction as TopToBottom and then save
diagram = Diagram(fileName)
flowChartOptions.setDirection(LayoutDirection.TOP_TO_BOTTOM)
diagram.layout(flowChartOptions)
diagram.save("sample_top_btm.vdx", SaveFileFormat.VDX)

# set layout direction as LeftToRight and then save
diagram = Diagram(fileName)
flowChartOptions.setDirection(LayoutDirection.LEFT_TO_RIGHT)
diagram.layout(flowChartOptions)
diagram.save("sample_left_right.vdx", SaveFileFormat.VDX)

# set layout direction as RightToLeft and then save
diagram = Diagram(fileName)
flowChartOptions.setDirection(LayoutDirection.RIGHT_TO_LEFT)
diagram.layout(flowChartOptions)
diagram.save("sample_right_left.vdx", SaveFileFormat.VDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
### **Laying Out Shapes in the Compact Tree Style**
The compact tree layout style tries to built a tree structure. It uses the same input file as the example above and saves out to several different compact tree styles.

|<p>**Compact tree layout - down and right** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_6.png)</p>|
| :- |
|<p>**Compact tree layout - down and left** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Compact tree layout - right and down** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Compact tree layout - left and down** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_9.png)</p>|
| :- | :- |
To layout shapes in the compact tree style:

1. Create an instance of the Diagram class.
1. Create an instance of the LayoutOptions class and set compact tree style properties.
1. Call the Diagram class' Layout method by passing LayoutOptions.
1. Call the the Diagram class' Save method to write the Visio file.
#### **Compact Tree Style Programming Sample**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

        
fileName = "LayOutShapesInCompactTreeStyle.vdx"
# load an existing Visio diagram
diagram = Diagram(fileName)

# set layout options 
compactTreeOptions = LayoutOptions()
compactTreeOptions.setLayoutStyle(LayoutStyle.COMPACT_TREE)
compactTreeOptions.setEnlargePage(True)

# set layout direction as DownThenRight and then save
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_RIGHT)
diagram.layout(compactTreeOptions)
diagram.save("sample_down_right.vdx", SaveFileFormat.VDX)

# set layout direction as DownThenLeft and then save
diagram = Diagram(fileName)
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_LEFT)
diagram.layout(compactTreeOptions)
diagram.save("sample_down_left.vdx", SaveFileFormat.VDX)

# set layout direction as RightThenDown and then save
diagram = Diagram(fileName)
compactTreeOptions.setDirection(LayoutDirection.RIGHT_THEN_DOWN)
diagram.layout(compactTreeOptions)
diagram.save("sample_right_down.vdx", SaveFileFormat.VDX)

# set layout direction as LeftThenDown and then save
diagram = Diagram(fileName)
compactTreeOptions.setDirection(LayoutDirection.LEFT_THEN_DOWN)
diagram.layout(compactTreeOptions)
diagram.save("sample_left_down.vdx", SaveFileFormat.VDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
## **Auto-fit the Visio Diagram**
Aspose.Diagram API supports auto-fitting of the Visio drawing. This feature operation helps to bring outside shapes inside the Visio page boundary.

Aspose.Diagram for Python via Java API has the Diagram class that represents a Visio drawing. The DiagramSaveOptions class exposes AutoFitPageToDrawingContent property to auto fit the Visio drawing.

This example work as follows:

1. Create an object of the Diagram class.
1. Create an object of the DiagramSaveOptions class and pass the resultant file format.
1. Set AutoFitPageToDrawingContent property of the DiagramSaveOptions object.
1. Call Save method of the Diagram class object and also pass complete file path and the DiagramSaveOptions object.
### **Auto-fit Programming Sample**
The following example code shows how to auto-fit shapes in the Visio diagram.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load a Visio diagram
diagram = Diagram("BFlowcht.vsdx")

# use saving options
options = DiagramSaveOptions(SaveFileFormat.VSDX)
# set Auto fit page property
options.setAutoFitPageToDrawingContent(True)

# save Visio diagram
diagram.save("AutoFitShapesInVisio_Out.vsdx", options)

jpype.shutdownJVM()

{{< /highlight >}}
```
## **Working with VBA Project**
### **Modify VBA Module Code in Visio Diagram**
This article demonstrates how to modify a VBA module code automatically using Aspose.Diagram for Python via Java.

We have added VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference and VbaProjectReferenceCollection classes. These classes help to get control over VBA project. Developers can extract and modify VBA module code.
### **Modify VBA Module Code Programming Sample**
Please check this code example:

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

diagram = Diagram("Macro.vsdm")
# extract VBA project
v = diagram.getVbaProject()
# Iterate through the modules and modify VBA macro code
for i in range(0, diagram.getVbaProject().getModules().getCount() - 1):
	module = diagram.getVbaProject().getModules().get(i)
	code = module.getCodes()
	if code.contains("This is test message."):
		code = code.replace("This is test message.", "This is Aspose.Diagram message.")
	module.setCodes(code)

# save the Visio diagram
diagram.save("out.vssm", SaveFileFormat.VSSM)

jpype.shutdownJVM()

{{< /highlight >}}
```
### **Remove All Macros from the Visio Diagram**
Aspose.Diagram for Python via Java allows developers to remove all macros from the Visio diagram.

The JavaProjectData property, exposed by the Diagram class, allows you to remove all macros from the Visio drawing.
### **Remove All Macros Programming Sample**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load a Visio diagram
diagram = Diagram("Macro.vsdm")

# remove all macros
diagram.setVbProjectData(None)

# Save diagram
diagram.save("RemoveMacrosFromVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```
