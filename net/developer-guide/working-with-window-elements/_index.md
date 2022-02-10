---
title: Working with Window Elements
type: docs
weight: 100
url: /net/working-with-window-elements/
description: This section explains get property of window elements in visio with Aspose.Diagram.
---

## **Retrieve Window Elements from the Visio Drawing**
The main Visio application window can contain any open Visio files, the same as modern web browsers allow for multiple tabbed web pages in one window. Developers can retrieve Window objects using [Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

The [WindowCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) object represents a list of [Window](http://www.aspose.com/api/net/diagram/aspose.diagram/window) objects available in the drawing. The Windows property, exposed by the Diagram class, supports a collection of Aspose.Diagram.Window objects. This property can be used to retrieve the window information that is, the Window ID, type, height, width and state.
### **Retrieve Window Elements Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Window-Elements-RetrieveWindowElementsOfDiagram-RetrieveWindowElementsOfDiagram.cs" >}}
## **Add Window Element to the Visio Diagram**
The main Visio application window can contain any open Visio files, the same as modern web browsers allow for multiple tabbed web pages in one window. Developers can now add a new Window object in a Microsoft Visio instance using [Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

The [Window](http://www.aspose.com/api/net/diagram/aspose.diagram/window) object represents an open window in a Microsoft Visio instance. The [Add](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection/methods/add) method, exposed by the [WindowCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) class, allows to add a new Window object.
### **Add Window Element Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Window-Elements-AddWindowElementInVisio-AddWindowElementInVisio.cs" >}}
## **Add Support of Dynamic Grids and Connection Points**
The dynamic grid helps you position new shapes vertically and horizontally relative to the shapes you've already placed in the drawing. Regarding the connection points, once marked as checked, will help us to see the connection points when we are in the process of connecting to them. We can achieve both options using [Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Support of Dynamic Grids and Connection Points in the Visio Drawings**
The [Window](http://www.aspose.com/api/net/diagram/aspose.diagram/window) class offers DynamicGridEnabled and ShowConnectionPoints properties. These properties can be used to apply settings to support dynamic grids and show connection points options.
#### **Add Support Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Window-Elements-AddSupportOfVisualAids-AddSupportOfVisualAids.cs" >}}
## **Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram**
Microsoft Office Visio has a pair of rulers, a grid, and two types of guides and page breaks flag to see what will be printed on each page. Developers can apply these settings using [Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/). The settings apply globally to a single page.

The [Window](http://www.aspose.com/api/net/diagram/aspose.diagram/window) class offers ShowGrid, ShowGuides, ShowRulers and ShowPageBreaks properties. These properties can be used to apply settings to show and hide grids, guides, rulers and page breaks.
### **Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Window-Elements-DisplayGridsRulersGuidesAndPageBreaks-DisplayGridsRulersGuidesAndPageBreaks.cs" >}}
