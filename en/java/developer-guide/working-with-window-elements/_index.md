---
title: Working with Window Elements
type: docs
weight: 130
url: /java/working-with-window-elements/
---

## **Retrieve Window Elements from the Visio Drawing**
The main Visio application window can contain any open Visio files, the same as modern web browsers allow for multiple tabbed web pages in one window. Developers can retrieve Window objects using [Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

The [WindowCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/windowcollection) object represents a list of [Window](https://reference.aspose.com/diagram/java/com.aspose.diagram/window) objects available in the drawing. The Windows property, exposed by the Diagram class, supports a collection of Aspose.Diagram.Window objects. This property can be used to retrieve the window information that is, the Window ID, type, height, width and state.

**A console window showing the output from the code.**

![todo:image_alt_text](http://i.imgur.com/zduARGh.png)
### **Retrieve Window Elements Programming Sample**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveWindowElementsOfDiagram.class);    
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// iterate through the window elements
for (Window window :(Iterable<Window>) diagram.getWindows())
{
    System.out.println("ID: " + window.getID());
    System.out.println("Type: " + window.getWindowType());
    System.out.println("Window height: " + window.getWindowHeight());
    System.out.println("Window width: " + window.getWindowWidth());
    System.out.println("Window state: " + window.getWindowState());
}

{{< /highlight >}}

## **Add Window Element to the Visio Diagram**
The main Visio application window can contain any open Visio files, the same as modern web browsers allow for multiple tabbed web pages in one window. Developers can now add a new Window object in a Microsoft Visio instance using [Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

The Window object represents an open window in a Microsoft Visio instance. The Add method, exposed by the WindowCollection class, allows to add a new Window object.
### **Add Window Element Programming Sample**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWindowElementInVisio.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// initialize window object
Window window = new Window();
// set window state
window.setWindowState(WindowStateValue.MAXIMIZED);
// set window height
window.setWindowHeight(500);
// set window width
window.setWindowWidth(500);
// set window type
window.setWindowType(WindowTypeValue.STENCIL);
// add window object
diagram.getWindows().add(window);

// save in any supported format
diagram.save(dataDir + "AddWindowElementInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Add Support of Dynamic Grids and Connection Points**
The dynamic grid helps you position new shapes vertically and horizontally relative to the shapes you've already placed in the drawing. Regarding the connection points, once marked as checked, will help us to see the connection points when we are in the process of connecting to them. We can achieve both options using [Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).
### **Support of Dynamic Grids and Connection Points in the Visio Drawings**
The Window class offers DynamicGridEnabled and ShowConnectionPoints properties. These properties can be used to apply settings to support dynamic grids and show connection points options.

**A Visio application showing the options in Visio.**

![todo:image_alt_text](http://i.imgur.com/bxsJIwF.png)
#### **Add Support Programming Sample**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddSupportOfVisualAids.class);
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// check dynamic grid option
window.setDynamicGridEnabled(BOOL.TRUE);
// check connection points option
window.setShowConnectionPoints(BOOL.TRUE);
        
// save visio drawing
diagram.save(dataDir + "AddSupportOfVisualAids_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram**
Microsoft Office Visio has a pair of rulers, a grid, and two types of guides and page breaks flag to see what will be printed on each page. Developers can apply these settings using [Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/). The settings apply globally to a single page.

The Window class offers ShowGrid, ShowGuides, ShowRulers and ShowPageBreaks properties. These properties can be used to apply settings to show and hide grids, guides, rulers and page breaks.

**A Visio application showing the options in Visio.**

![todo:image_alt_text](http://i.imgur.com/E0pvXbP.png)
### **Programming Sample**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DisplayGridsRulersGuidesAndPageBreaks.class);     
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// set visibility of grid
window.setShowGrid(BOOL.TRUE);
// set visibility of guides
window.setShowGuides(BOOL.TRUE);
// set visibility of rulers
window.setShowRulers(BOOL.TRUE);
// set visibility of page breaks
window.setShowPageBreaks(BOOL.TRUE);

// save diagram
diagram.save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

