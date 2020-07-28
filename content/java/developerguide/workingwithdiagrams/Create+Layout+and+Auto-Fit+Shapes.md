+++
title = "Create Layout and Auto-Fit Shapes" 
description = "" 
weight = 12023 
+++

Aspose.Diagram for Java : Create, Layout and Auto-Fit Shapes  

# Aspose.Diagram for Java : Create, Layout and Auto-Fit Shapes


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Creating a Diagram](#Create,LayoutandAuto-FitShapes-CreatingaDiagram)
    *   1.1 [Programming Sample](#Create,LayoutandAuto-FitShapes-ProgrammingSample)
*   2 [Layout Shapes in Flowchart Style](#Create,LayoutandAuto-FitShapes-LayoutShapesinFlowchartStyle)
    *   2.1 [Flowchart Style Programming Sample](#Create,LayoutandAuto-FitShapes-FlowchartStyleProgrammingSample)
    *   2.2 [Laying Out Shapes in the Compact Tree Style](#Create,LayoutandAuto-FitShapes-LayingOutShapesintheCompactTreeStyle)
        *   2.2.1 [Compact Tree Style Programming Sample](#Create,LayoutandAuto-FitShapes-CompactTreeStyleProgrammingSample)
*   3 [Auto-fit the Visio Diagram](#Create,LayoutandAuto-FitShapes-Auto-fittheVisioDiagram)
    *   3.1 [Auto-fit Programming Sample](#Create,LayoutandAuto-FitShapes-Auto-fitProgrammingSample)
*   4 [Working with VBA Project](#Create,LayoutandAuto-FitShapes-WorkingwithVBAProject)
    *   4.1 [Modify VBA Module Code in Visio Diagram](#Create,LayoutandAuto-FitShapes-ModifyVBAModuleCodeinVisioDiagram)
    *   4.2 [Modify VBA Module Code Programming Sample](#Create,LayoutandAuto-FitShapes-ModifyVBAModuleCodeProgrammingSample)
    *   4.3 [Remove All Macros from the Visio Diagram](#Create,LayoutandAuto-FitShapes-RemoveAllMacrosfromtheVisioDiagram)
    *   4.4 [Remove All Macros Programming Sample](#Create,LayoutandAuto-FitShapes-RemoveAllMacrosProgrammingSample)
{{< /panel >}}
 

 

## Creating a Diagram

Aspose.Diagram for Java lets you read and create Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. The first step when creating new documents, is to create a diagram. Then [add shapes and connectors](https://docs2.aspose.com/diagram/java/developerguide/technicalarticles/add+and+connect+visio+shapes) to build up the diagram. Use the default constructor of [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class to create a new diagram.

### Programming Sample

## Layout Shapes in Flowchart Style

With certain types of connected drawings, such as flowcharts and network diagrams, you can use the **Layout Shapes** feature to automatically position shapes. Automatically positioning is faster than manually dragging each shape to a new location.

For example, if you're updating a large flowchart to include a new process, you can add and connect the shapes that make up the process, and then use the layout feature to automatically layout the updated drawing.

The `Layout` method, exposed by the [`Diagram`](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class layouts the shapes and/or reroutes the connectors on all the diagram's pages. This method accepts an [LayoutOptions](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Layoutoptions) object as an argument. Use the different properties exposed by the `LayoutOptions` class to automatically layout shapes.

The image below shows the diagram loaded by the code snippets in this article, before auto layout is applied. The code snippets show how to apply [flowchart layouts](https://docs2.aspose.com/diagram/java/developerguide/workingwithdiagrams/create+layout+and+auto-fit+shapes) and [compact tree layouts](https://docs2.aspose.com/diagram/java/developerguide/workingwithdiagrams/create+layout+and+auto-fit+shapes).

**The source diagram.**  
![](https://docs2.aspose.com/diagram/java/attachments/18612235/18809123.png)

The code snippets in this article takes the source diagram and applies several types of auto layout to it, saving each in a separate file.

**Layout shapes bottom to top**  
![](https://docs2.aspose.com/diagram/java/attachments/18612235/18809124.png)

**Layout shapes top to bottom**  
![](https://docs2.aspose.com/diagram/java/attachments/18612235/18809125.png)

**Layout shapes left to right**  
![](https://docs2.aspose.com/diagram/java/attachments/18612235/18809126.png)

**Layout shapes right to left**  
![](https://docs2.aspose.com/diagram/java/attachments/18612235/18809127.png)

To layout shapes in flowchart style:

1.  Create an instance of the `Diagram` class.
2.  Create an instance of `LayoutOptions` class and set Flowchart style related properties.
3.  Call the `Diagram` class' `Layout` method by passing `LayoutOptions`.
4.  Call the `Diagram` class' `Save` method to write the Visio drawing.

### Flowchart Style Programming Sample

### Laying Out Shapes in the Compact Tree Style

The compact tree layout style tries to built a tree structure. It uses the same input file as the [example above](https://docs2.aspose.com/diagram/java/developerguide/workingwithdiagrams/create+layout+and+auto-fit+shapes) and saves out to several different compact tree styles.

**Compact tree layout - down and right**  
![](https://docs2.aspose.com/diagram/java/attachments/18612235/18809128.png)

**Compact tree layout - down and left**  
![](https://docs2.aspose.com/diagram/java/attachments/18612235/18809129.png)

**Compact tree layout - right and down**  
![](https://docs2.aspose.com/diagram/java/attachments/18612235/18809130.png)

**Compact tree layout - left and down**  
![](https://docs2.aspose.com/diagram/java/attachments/18612235/18809131.png)

To layout shapes in the compact tree style:

1.  Create an instance of the [`Diagram`](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class.
2.  Create an instance of the `LayoutOptions` class and set compact tree style properties.
3.  Call the `Diagram` class' `Layout` method by passing `LayoutOptions`.
4.  Call the the `Diagram` class' `Save` method to write the Visio file.

#### Compact Tree Style Programming Sample

## Auto-fit the Visio Diagram

Aspose.Diagram API supports auto-fitting of the Visio drawing. This feature operation helps to bring outside shapes inside the Visio page boundary.

Aspose.Diagram for Java API has the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class that represents a Visio drawing. The [DiagramSaveOptions](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/diagramsaveoptions) class exposes `AutoFitPageToDrawingContent` property to auto fit the Visio drawing.

This example work as follows:

1.  Create an object of the `Diagram` class.
2.  Create an object of the `DiagramSaveOptions` class and pass the resultant file format.
3.  Set `AutoFitPageToDrawingContent` property of the `DiagramSaveOptions` object.
4.  Call `Save` method of the Diagram class object and also pass complete file path and the `DiagramSaveOptions` object.

### Auto-fit Programming Sample

The following example code shows how to auto-fit shapes in the Visio diagram.

## Working with VBA Project

### Modify VBA Module Code in Visio Diagram

This article demonstrates how to modify a VBA module code automatically using Aspose.Diagram for Java.

We have added `VbaModule`, `VbaModuleCollection`, `VbaProject`, `VbaProjectReference` and `VbaProjectReferenceCollection` classes. These classes help to get control over VBA project. Developers can extract and modify VBA module code.

### Modify VBA Module Code Programming Sample

Please check this code example:

### Remove All Macros from the Visio Diagram

Aspose.Diagram for Java allows developers to remove all macros from the Visio diagram.

The `JavaProjectData` property, exposed by the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Diagram) class, allows you to remove all macros from the Visio drawing.

### Remove All Macros Programming Sample

## Attachments:

![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [CompactTreeLeftDown.png](https://docs2.aspose.com/diagram/java/attachments/18612235/18809131.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [CompactTreeRightDown.png](https://docs2.aspose.com/diagram/java/attachments/18612235/18809130.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [CompactTreeDownLeft.png](https://docs2.aspose.com/diagram/java/attachments/18612235/18809129.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [CompactTreeDownRight.png](https://docs2.aspose.com/diagram/java/attachments/18612235/18809128.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [FlowchartRightLeft.png](https://docs2.aspose.com/diagram/java/attachments/18612235/18809127.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [FlowchartLeftRight.png](https://docs2.aspose.com/diagram/java/attachments/18612235/18809126.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [FlowchartTopBottom.png](https://docs2.aspose.com/diagram/java/attachments/18612235/18809125.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [FlowchartBottomTop.png](https://docs2.aspose.com/diagram/java/attachments/18612235/18809124.png) (image/png)  
![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [BeforeLayout.png](https://docs2.aspose.com/diagram/java/attachments/18612235/18809123.png) (image/png)  

