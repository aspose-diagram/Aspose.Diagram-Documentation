---
title: Arbeta med fönsterelement
type: docs
weight: 100
url: /sv/net/working-with-window-elements/
description: Det här avsnittet förklarar get-egenskapen för fönsterelement i visio med Aspose.Diagram.
---
## **Hämta fönsterelement från Visio-ritningen**
 Huvudapplikationsfönstret Visio kan innehålla alla öppna Visio-filer, på samma sätt som moderna webbläsare tillåter flera webbsidor med flikar i ett fönster. Utvecklare kan hämta Window-objekt med hjälp av[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 De[Window Collection](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) objekt representerar en lista över[Fönster](http://www.aspose.com/api/net/diagram/aspose.diagram/window)objekt som finns på ritningen. Egenskapen Windows, exponerad av klassen Diagram, stöder en samling Aspose.Diagram.Window-objekt. Den här egenskapen kan användas för att hämta fönsterinformationen, dvs fönster-ID, typ, höjd, bredd och tillstånd.
### **Hämta programmeringsexempel för fönsterelement**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Iterate through the window elements
foreach (Window window in diagram.Windows)
{
    Console.WriteLine("ID: " + window.ID);
    Console.WriteLine("Type: " + window.WindowType);
    Console.WriteLine("Window height: " + window.WindowHeight);
    Console.WriteLine("Window width: " + window.WindowWidth);
    Console.WriteLine("Window state: " + window.WindowState);
}

{{< /highlight >}}
```
## **Lägg till Window Element till Visio Diagram**
 Huvudapplikationsfönstret Visio kan innehålla alla öppna Visio-filer, på samma sätt som moderna webbläsare tillåter flera webbsidor med flikar i ett fönster. Utvecklare kan nu lägga till ett nytt Window-objekt i en Microsoft Visio-instans med hjälp av[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 De[Fönster](http://www.aspose.com/api/net/diagram/aspose.diagram/window) objekt representerar ett öppet fönster i en Microsoft Visio-instans. De[Lägg till](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection/methods/add) metod, exponerad av[Window Collection](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) klass, tillåter att lägga till ett nytt Window-objekt.
### **Lägg till programmeringsexempel för fönsterelement**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Initialize window object
Window window = new Window();
// Set window state
window.WindowState = WindowStateValue.Maximized;
// Set window height
window.WindowHeight = 500;
// Set window width
window.WindowWidth = 500;
// Set window type
window.WindowType = WindowTypeValue.Stencil;
// Add window object
diagram.Windows.Add(window);

// Save in any supported format
diagram.Save(dataDir + "AddWindowElementInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Lägg till stöd för dynamiska nät och anslutningspunkter**
Det dynamiska rutnätet hjälper dig att placera nya former vertikalt och horisontellt i förhållande till de former du redan har placerat i ritningen. När det gäller anslutningspunkterna, när de är markerade som markerade, kommer det att hjälpa oss att se anslutningspunkterna när vi håller på att ansluta till dem. Vi kan uppnå båda alternativen med hjälp av[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Stöd för dynamiska nät och anslutningspunkter i Visio-ritningarna**
 De[Fönster](http://www.aspose.com/api/net/diagram/aspose.diagram/window) class erbjuder egenskaperna DynamicGridEnabled och ShowConnectionPoints. Dessa egenskaper kan användas för att tillämpa inställningar för att stödja dynamiska rutnät och visa alternativ för anslutningspunkter.
#### **Lägg till supportprogrammeringsexempel**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Check dynamic grid option
window.DynamicGridEnabled = BOOL.True;
// Check connection points option
window.ShowConnectionPoints = BOOL.True;
            
// Save visio drawing
diagram.Save(dataDir + "AddSupportOfVisualAids_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Visa och dölj rutnät, linjaler, guider och sidbrytningar i Visio Diagram**
 Microsoft Office Visio har ett par linjaler, ett rutnät och två typer av stödlinjer och sidbrytningsflagga för att se vad som kommer att skrivas ut på varje sida. Utvecklare kan tillämpa dessa inställningar med hjälp av[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/)Inställningarna gäller globalt för en enda sida.

 De[Fönster](http://www.aspose.com/api/net/diagram/aspose.diagram/window)klass erbjuder egenskaperna ShowGrid, ShowGuides, ShowRulers och ShowPageBreaks. Dessa egenskaper kan användas för att tillämpa inställningar för att visa och dölja rutnät, stödlinjer, linjaler och sidbrytningar.
### **Programmeringsexempel**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Set visibility of grid
window.ShowGrid = BOOL.True;
// Set visibility of guides
window.ShowGuides = BOOL.True;
// Set visibility of rulers
window.ShowRulers = BOOL.True;
// Set visibility of page breaks
window.ShowPageBreaks = BOOL.True;

// Save diagram
diagram.Save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
