---
title: Arbeta med fönsterelement
type: docs
weight: 130
url: /sv/java/working-with-window-elements/
---
## **Hämta fönsterelement från Visio-ritningen**
 Huvudapplikationsfönstret Visio kan innehålla alla öppna Visio-filer, på samma sätt som moderna webbläsare tillåter flera webbsidor med flikar i ett fönster. Utvecklare kan hämta Window-objekt med hjälp av[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 De[Window Collection](https://reference.aspose.com/diagram/java/com.aspose.diagram/windowcollection) objekt representerar en lista över[Fönster](https://reference.aspose.com/diagram/java/com.aspose.diagram/window)objekt som finns på ritningen. Egenskapen Windows, exponerad av klassen Diagram, stöder en samling Aspose.Diagram.Window-objekt. Den här egenskapen kan användas för att hämta fönsterinformationen, dvs fönster-ID, typ, höjd, bredd och tillstånd.

**Ett konsolfönster som visar utdata från koden.**

![todo:image_alt_text](http://i.imgur.com/zduARGh.png)
### **Hämta programmeringsexempel för fönsterelement**
```
{{< highlight "java" >}}
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
```
## **Lägg till Window Element till Visio Diagram**
 Huvudapplikationsfönstret Visio kan innehålla alla öppna Visio-filer, på samma sätt som moderna webbläsare tillåter flera webbsidor med flikar i ett fönster. Utvecklare kan nu lägga till ett nytt Window-objekt i en Microsoft Visio-instans med hjälp av[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

Window-objektet representerar ett öppet fönster i en Microsoft Visio-instans. Add-metoden, exponerad av WindowCollection-klassen, tillåter att lägga till ett nytt Window-objekt.
### **Lägg till programmeringsexempel för fönsterelement**
```
{{< highlight "java" >}}
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
```
## **Lägg till stöd för dynamiska nät och anslutningspunkter**
Det dynamiska rutnätet hjälper dig att placera nya former vertikalt och horisontellt i förhållande till de former du redan har placerat i ritningen. När det gäller anslutningspunkterna, när de är markerade som markerade, kommer det att hjälpa oss att se anslutningspunkterna när vi håller på att ansluta till dem. Vi kan uppnå båda alternativen med hjälp av[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).
### **Stöd för dynamiska nät och anslutningspunkter i Visio-ritningarna**
Window-klassen erbjuder egenskaperna DynamicGridEnabled och ShowConnectionPoints. Dessa egenskaper kan användas för att tillämpa inställningar för att stödja dynamiska rutnät och visa alternativ för anslutningspunkter.

**En Visio-applikation som visar alternativen i Visio.**

![todo:image_alt_text](http://i.imgur.com/bxsJIwF.png)
#### **Lägg till supportprogrammeringsexempel**
```
{{< highlight "java" >}}
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
```
## **Visa och dölj rutnät, linjaler, guider och sidbrytningar i Visio Diagram**
 Microsoft Office Visio har ett par linjaler, ett rutnät och två typer av stödlinjer och sidbrytningsflagga för att se vad som kommer att skrivas ut på varje sida. Utvecklare kan tillämpa dessa inställningar med hjälp av[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)Inställningarna gäller globalt för en enda sida.

Window-klassen erbjuder egenskaperna ShowGrid, ShowGuides, ShowRulers och ShowPageBreaks. Dessa egenskaper kan användas för att tillämpa inställningar för att visa och dölja rutnät, stödlinjer, linjaler och sidbrytningar.

**En Visio-applikation som visar alternativen i Visio.**

![todo:image_alt_text](http://i.imgur.com/E0pvXbP.png)
### **Programmeringsexempel**
```
{{< highlight "java" >}}
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
```
