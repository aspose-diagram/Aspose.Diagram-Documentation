---
title : "Create Update Layout and Auto-Fit Shapes" 
description : "" 
weight : 12019 
toc : false
type: docs
url: /net/developerguide/workingwithdiagrams/create+update+layout+and+auto-fit+shapes/
---

# Aspose.Diagram for .NET : Create, Update, Layout and Auto-Fit Shapes


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
*   5 [Creating a New Diagram with VSTO](#creating-a-new-diagram-with-vsto)
    *   5.1 [Create New Diagram with VSTO Programming Sample](#create-new-diagram-with-vsto-programming-sample)
*   6 [Creating a New Diagram with Aspose.Diagram for .NET](#creating-a-new-diagram-with-aspose.diagram-for-.net)
    *   6.1 [New Diagram with Aspose.Diagram for .NET Programming Sample](#new-diagram-with-aspose.diagram-for-.net-programming-sample)
*   7 [Update Shape Properties](#update-shape-properties)
    *   7.1 [Updating Shape Properties with VSTO](#updating-shape-properties-with-vsto)
        *   7.1.1 [Updating Shape Properties with VSTO Programming Sample](#updating-shape-properties-with-vsto-programming-sample)
    *   7.2 [Updating Shape Properties with Aspose.Diagram for .NET](#updating-shape-properties-with-aspose.diagram-for-.net)
        *   7.2.1 [Updating Shape Properties with Aspose.Diagram for .NET Programming Sample](#updating-shape-properties-with-aspose.diagram-for-.net-programming-sample)
{{< /panel >}}
 

 

## Creating a Diagram

Aspose.Diagram for .NET lets you read and create Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. The first step when creating new documents, is to create a diagram. Then [add shapes and connectors](/pages/createpage.action?spaceKey=diagramnet&title=Add+and+Connect+Visio+Shapes&linkCreation=true&fromPageId=18350161) to build up the diagram. Use the default constructor of [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class to create a new diagram.

### Programming Sample

## Layout Shapes in Flowchart Style

With certain types of connected drawings, such as flowcharts and network diagrams, you can use the **Layout Shapes** feature to automatically position shapes. Automatically positioning is faster than manually dragging each shape to a new location.

For example, if you're updating a large flowchart to include a new process, you can add and connect the shapes that make up the process, and then use the layout feature to automatically layout the updated drawing.

The `Layout` method, exposed by the [`Diagram`](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class layouts the shapes and/or reroutes the connectors on all the diagram's pages. This method accepts an [LayoutOptions](http://www.aspose.com/api/net/diagram/aspose.diagram/layoutoptions) object as an argument. Use the different properties exposed by the `LayoutOptions` class to automatically layout shapes.

The image below shows the diagram loaded by the code snippets in this article, before auto layout is applied. The code snippets show how to apply [flowchart layouts](https://docs2.aspose.com/diagram/net/developerguide/workingwithdiagrams/create+update+layout+and+auto-fit+shapes) and [compact tree layouts](https://docs2.aspose.com/diagram/net/developerguide/workingwithdiagrams/create+update+layout+and+auto-fit+shapes).

**The source diagram.**  
![](https://docs2.aspose.com/diagram/net/attachments/18350161/18546951.png)

The code snippets in this article takes the source diagram and applies several types of auto layout to it, saving each in a separate file.

**Layout shapes bottom to top**  
![](https://docs2.aspose.com/diagram/net/attachments/18350161/18546952.png)

**Layout shapes top to bottom**  
![](https://docs2.aspose.com/diagram/net/attachments/18350161/18546949.png)

**Layout shapes left to right**  
![](https://docs2.aspose.com/diagram/net/attachments/18350161/18546950.png)

**Layout shapes right to left**  
![](https://docs2.aspose.com/diagram/net/attachments/18350161/18546947.png)

To layout shapes in flowchart style:

1.  Create an instance of the `Diagram` class.
2.  Create an instance of `LayoutOptions` class and set Flowchart style related properties.
3.  Call the `Diagram` class' `Layout` method by passing `LayoutOptions`.
4.  Call the `Diagram` class' `Save` method to write the Visio drawing.

### Flowchart Style Programming Sample

### Laying Out Shapes in the Compact Tree Style

The compact tree layout style tries to built a tree structure. It uses the same input file as the [example above](https://docs2.aspose.com/diagram/net/developerguide/workingwithdiagrams/create+update+layout+and+auto-fit+shapes) and saves out to several different compact tree styles.

**Compact tree layout - down and right**  
![](https://docs2.aspose.com/diagram/net/attachments/18350161/18546948.png)

**Compact tree layout - down and left**  
![](https://docs2.aspose.com/diagram/net/attachments/18350161/18546945.png)

**Compact tree layout - right and down**  
![](https://docs2.aspose.com/diagram/net/attachments/18350161/18546946.png)

**Compact tree layout - left and down**  
![](https://docs2.aspose.com/diagram/net/attachments/18350161/18546928.png)

To layout shapes in the compact tree style:

1.  Create an instance of the [`Diagram`](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class.
2.  Create an instance of the `LayoutOptions` class and set compact tree style properties.
3.  Call the `Diagram` class' `Layout` method by passing `LayoutOptions`.
4.  Call the the `Diagram` class' `Save` method to write the Visio file.

#### Compact Tree Style Programming Sample

## Auto-fit the Visio Diagram

Aspose.Diagram API supports auto-fitting of the Visio drawing. This feature operation helps to bring outside shapes inside the Visio page boundary. Aspose.Diagram for .NET API has the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class that represents a Visio drawing. The [DiagramSaveOptions](http://www.aspose.com/api/net/diagram/aspose.diagram/diagramsaveoptions) class exposes `AutoFitPageToDrawingContent` property to auto fit the Visio drawing.

This example work as follows:

1.  Create an object of the `Diagram` class.
2.  Create an object of the `DiagramSaveOptions` class and pass the resultant file format.
3.  Set `AutoFitPageToDrawingContent` property of the `DiagramSaveOptions` object.
4.  Call `Save` method of the Diagram class object and also pass complete file path and the `DiagramSaveOptions` object.

### Auto-fit Programming Sample

The following example code shows how to auto-fit shapes in the Visio diagram.

## Working with VBA Project

### Modify VBA Module Code in Visio Diagram

This article demonstrates how to modify a VBA module code automatically using Aspose.Diagram for .NET. We have added [VbaModule](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [VbaModuleCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [VbaProject](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) and [VbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) classes. These classes help to get control over VBA project. Developers can extract and modify VBA module code.

### Modify VBA Module Code Programming Sample

Please check this code example:

### Remove All Macros from the Visio Diagram

Aspose.Diagram for .NET allows developers to remove all macros from the Visio diagram. The `VbProjectData` property, exposed by the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, allows you to remove all macros from the Visio drawing.

### Remove All Macros Programming Sample

## Creating a New Diagram with VSTO

[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) lets developers to create and work with Microsoft Office Visio diagrams and incorporate features in their software applications. There are other ways of working with Visio files, most commonly, Microsoft Automation. Unfortunately, that has some limitations. Aspose.Diagram is powerful and fast and works independently without Microsoft Office installation.

This migration article shows how to use first [VSTO](https://docs2.aspose.com/diagram/net/developerguide/workingwithdiagrams/create+update+layout+and+auto-fit+shapes) and then [Aspose.Diagram for .NET](https://docs2.aspose.com/diagram/net/developerguide/workingwithdiagrams/create+update+layout+and+auto-fit+shapes) to create a new diagram and add some shapes to it. You'll notice that the Aspose.Diagram code is shorter than VSTO code. Feel free to use the code as a base for your own development and enhance it to meet your needs. VSTO lets you program with Microsoft Visio files. To create a new diagram:

1.  Create a Visio application object.
2.  Make the application object invisible.
3.  Create an empty diagram.
4.  Add shapes from Visio masters (stencils).
5.  Save the file as VDX.

### Create New Diagram with VSTO Programming Sample

using Visio = Microsoft.Office.Interop.Visio;  
Imports Visio = Microsoft.Office.Interop.Visio

**  
Example:**

## Creating a New Diagram with Aspose.Diagram for .NET

Using Aspose.Diagram API, developers don't need Microsoft Office Visio installation on the machine, and they can work independently of Microsoft Office Automation.

To create a new diagram:

1.  Create an empty diagram.
2.  Add shapes from Visio masters (stencils).
3.  Save the file as VDX.

### New Diagram with Aspose.Diagram for .NET Programming Sample

using Aspose.Diagram;  
Imports Aspose.Diagram

Example:

## Update Shape Properties

When working with Microsoft Visio diagrams, users can update shape attributes including text, style, position, height and width. As a software developer working with Visio files, you'll be asked to do this programmatically. The good news is that it is possible, either using the mechanisms for programming with Visio files that Microsoft provides, VSTO, or using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx).

Below topic shows how to use [VSTO](https://docs2.aspose.com/diagram/net/developerguide/workingwithdiagrams/create+update+layout+and+auto-fit+shapes) and [Aspose.Diagram](https://docs2.aspose.com/diagram/net/developerguide/workingwithdiagrams/create+update+layout+and+auto-fit+shapes) to update shape properties. The code snippets below show how to update shape properties for VSTO and Aspose.Diagram for .NET. Feel free to use the code and apply it to your particular situation.

### Updating Shape Properties with VSTO

VSTO lets you program with Microsoft Visio files. To update shape properties:

1.  Create a Visio application object.
2.  Make the application object invisible.
3.  Open an existing Visio VSD file.
4.  Find the required shape.
5.  Update the shape properties (text, text style, position and size).
6.  Save the file as VDX.

#### Updating Shape Properties with VSTO Programming Sample

using Visio = Microsoft.Office.Interop.Visio;  
Imports Visio = Microsoft.Office.Interop.Visio

**Example:**

### Updating Shape Properties with Aspose.Diagram for .NET

Using Aspose.Diagram API, developers don't need Microsoft Office Visio on the machine, and they can work independently of Microsoft Office Automation.

To update shape properties with Aspose.Diagram for .NET:

1.  Open an existing Visio VSD file.
2.  Find the required shape.
3.  Update the shape properties (text, text style, position and size).
4.  Save the file as VDX.

#### Updating Shape Properties with Aspose.Diagram for .NET Programming Sample

using Aspose.Diagram;  
Imports Aspose.Diagram

**Example:**

## Attachments:

![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [BeforeLayout.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546951.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [FlowchartBottomTop.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546952.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [FlowchartTopBottom.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546949.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [FlowchartLeftRight.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546950.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [FlowchartRightLeft.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546947.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [CompactTreeDownRight.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546948.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [CompactTreeDownLeft.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546945.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [CompactTreeRightDown.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546946.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [CompactTreeLeftDown.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546928.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Export diagrams to XML formats (VDX, VTX or VSX)-001.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546927.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Export diagrams to XML formats (VDX, VTX or VSX)-002.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546926.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Export diagrams to XML formats (VDX, VTX or VSX)-003.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546925.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Export diagrams to XML formats (VDX, VTX or VSX)-004.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546924.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Export diagrams to XML formats (VDX, VTX or VSX)-005.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546923.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Export diagrams to XML formats (VDX, VTX or VSX)-006.png](https://docs2.aspose.com/diagram/net/attachments/18350161/18546922.png) (image/png)  

