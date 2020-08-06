---
title : "Create Layout and Auto-Fit Shapes" 
description : "" 
weight : 12023 
toc : false
type: docs
url: /java/developerguide/workingwithdiagrams/create+layout+and+auto-fit+shapes/
---

# Aspose.Diagram for Java : Create, Layout and Auto-Fit Shapes


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Creating a Diagram](#creating-a-diagram)
    *   1.1 [Programming Sample](#programming-sample)
*   2 [Layout Shapes in Flowchart Style](#layout-shapes-in-flowchart-style)
    *   2.1 [Flowchart Style Programming Sample](#flowchart-style-programming-sample)
    *   2.2 [Laying Out Shapes in the Compact Tree Style](#laying-out-shapes-in-the-compact-tree-style)
        *   2.2.1 [Compact Tree Style Programming Sample](#compact-tree-style-programming-sample)
*   3 [Auto-fit the Visio Diagram](#auto-fit-the-visio-diagram)
    *   3.1 [Auto-fit Programming Sample](#auto-fit-programming-sample)
*   4 [Working with VBA Project](#working-with-vba-project)
    *   4.1 [Modify VBA Module Code in Visio Diagram](#modify-vba-module-code-in-visio-diagram)
    *   4.2 [Modify VBA Module Code Programming Sample](#modify-vba-module-code-programming-sample)
    *   4.3 [Remove All Macros from the Visio Diagram](#remove-all-macros-from-the-visio-diagram)
    *   4.4 [Remove All Macros Programming Sample](#remove-all-macros-programming-sample)
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
![image](18809123.png)

The code snippets in this article takes the source diagram and applies several types of auto layout to it, saving each in a separate file.

**Layout shapes bottom to top**  
![image](18809124.png)

**Layout shapes top to bottom**  
![image](18809125.png)

**Layout shapes left to right**  
![image](18809126.png)

**Layout shapes right to left**  
![image](18809127.png)

To layout shapes in flowchart style:

1.  Create an instance of the `Diagram` class.
2.  Create an instance of `LayoutOptions` class and set Flowchart style related properties.
3.  Call the `Diagram` class' `Layout` method by passing `LayoutOptions`.
4.  Call the `Diagram` class' `Save` method to write the Visio drawing.

### Flowchart Style Programming Sample

### Laying Out Shapes in the Compact Tree Style

The compact tree layout style tries to built a tree structure. It uses the same input file as the [example above](https://docs2.aspose.com/diagram/java/developerguide/workingwithdiagrams/create+layout+and+auto-fit+shapes) and saves out to several different compact tree styles.

**Compact tree layout - down and right**  
![image](18809128.png)

**Compact tree layout - down and left**  
![image](18809129.png)

**Compact tree layout - right and down**  
![image](18809130.png)

**Compact tree layout - left and down**  
![image](18809131.png)

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

