---
title: Create, Layout and Auto-Fit Shapes
type: docs
weight: 10
url: /java/create-layout-and-auto-fit-shapes/
---

## **Creating a Diagram**
Aspose.Diagram for Java lets you read and create Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. The first step when creating new documents, is to create a diagram. Then [add shapes and connectors](/diagram/java/add-and-connect-visio-shapes-html/) to build up the diagram. Use the default constructor of [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class to create a new diagram.
### **Programming Sample**
{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-CreateDiagram-CreateDiagram.java" >}}
## **Layout Shapes in Flowchart Style**
With certain types of connected drawings, such as flowcharts and network diagrams, you can use the **Layout Shapes** feature to automatically position shapes. Automatically positioning is faster than manually dragging each shape to a new location.

For example, if you're updating a large flowchart to include a new process, you can add and connect the shapes that make up the process, and then use the layout feature to automatically layout the updated drawing.

The Layout method, exposed by the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class layouts the shapes and/or reroutes the connectors on all the diagram's pages. This method accepts an [LayoutOptions](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Layoutoptions) object as an argument. Use the different properties exposed by the LayoutOptions class to automatically layout shapes.

The image below shows the diagram loaded by the code snippets in this article, before auto layout is applied. The code snippets show how to apply [flowchart layouts](/diagram/java/create-2c-layout-and-auto-fit-shapes-html/) and [compact tree layouts](/diagram/java/create-2c-layout-and-auto-fit-shapes-html/).

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
{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-LayOutShapesInFlowchartStyle-LayOutShapesInFlowchartStyle.java" >}}
### **Laying Out Shapes in the Compact Tree Style**
The compact tree layout style tries to built a tree structure. It uses the same input file as the [example above](/diagram/java/create-2c-layout-and-auto-fit-shapes-html/) and saves out to several different compact tree styles.

|<p>**Compact tree layout - down and right** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_6.png)</p>|
| :- |
|<p>**Compact tree layout - down and left** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Compact tree layout - right and down** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Compact tree layout - left and down** </p><p>![todo:image_alt_text](create-layout-and-auto-fit-shapes_9.png)</p>|
| :- | :- |
To layout shapes in the compact tree style:

1. Create an instance of the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class.
1. Create an instance of the LayoutOptions class and set compact tree style properties.
1. Call the Diagram class' Layout method by passing LayoutOptions.
1. Call the the Diagram class' Save method to write the Visio file.
#### **Compact Tree Style Programming Sample**
{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-LayOutShapesInCompactTreeStyle-LayOutShapesInCompactTreeStyle.java" >}}
## **Auto-fit the Visio Diagram**
Aspose.Diagram API supports auto-fitting of the Visio drawing. This feature operation helps to bring outside shapes inside the Visio page boundary.

Aspose.Diagram for Java API has the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class that represents a Visio drawing. The [DiagramSaveOptions](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/diagramsaveoptions) class exposes AutoFitPageToDrawingContent property to auto fit the Visio drawing.

This example work as follows:

1. Create an object of the Diagram class.
1. Create an object of the DiagramSaveOptions class and pass the resultant file format.
1. Set AutoFitPageToDrawingContent property of the DiagramSaveOptions object.
1. Call Save method of the Diagram class object and also pass complete file path and the DiagramSaveOptions object.
### **Auto-fit Programming Sample**
The following example code shows how to auto-fit shapes in the Visio diagram.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-AutoFitShapesInVisio-AutoFitShapesInVisio.java" >}}
## **Working with VBA Project**
### **Modify VBA Module Code in Visio Diagram**
This article demonstrates how to modify a VBA module code automatically using Aspose.Diagram for Java.

We have added VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference and VbaProjectReferenceCollection classes. These classes help to get control over VBA project. Developers can extract and modify VBA module code.
### **Modify VBA Module Code Programming Sample**
Please check this code example:

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-ModifyVBAModuleCode-ModifyVBAModuleCode.java" >}}
### **Remove All Macros from the Visio Diagram**
Aspose.Diagram for Java allows developers to remove all macros from the Visio diagram.

The JavaProjectData property, exposed by the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class, allows you to remove all macros from the Visio drawing.
### **Remove All Macros Programming Sample**
{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RemoveMacrosFromVisio-RemoveMacrosFromVisio.java" >}}
