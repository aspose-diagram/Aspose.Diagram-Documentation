---
title: Trabajar con elementos de ventana
type: docs
weight: 100
url: /es/net/working-with-window-elements/
description: Esta sección explica cómo obtener la propiedad de los elementos de la ventana en visio con Aspose.Diagram.
---
## **Recuperar elementos de ventana del dibujo Visio**
 La ventana principal de la aplicación Visio puede contener cualquier archivo Visio abierto, al igual que los navegadores web modernos permiten múltiples páginas web con pestañas en una ventana. Los desarrolladores pueden recuperar objetos de Windows usando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 los[VentanaColección](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) objeto representa una lista de[Ventana](http://www.aspose.com/api/net/diagram/aspose.diagram/window)objetos disponibles en el dibujo. La propiedad Windows, expuesta por la clase Diagram, admite una colección de objetos Aspose.Diagram.Window. Esta propiedad se puede utilizar para recuperar la información de la ventana, es decir, el ID de la ventana, el tipo, la altura, el ancho y el estado.
### **Recuperar muestra de programación de elementos de ventana**
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
## **Agregar elemento de ventana al Visio Diagram**
 La ventana principal de la aplicación Visio puede contener cualquier archivo Visio abierto, al igual que los navegadores web modernos permiten múltiples páginas web con pestañas en una ventana. Los desarrolladores ahora pueden agregar un nuevo objeto de ventana en una instancia Microsoft Visio usando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 los[Ventana](http://www.aspose.com/api/net/diagram/aspose.diagram/window) El objeto representa una ventana abierta en una instancia Microsoft Visio. los[Agregar](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection/methods/add) método, expuesto por la[VentanaColección](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) clase, permite agregar un nuevo objeto Ventana.
### **Agregar muestra de programación de elemento de ventana**
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
## **Agregar soporte de cuadrículas dinámicas y puntos de conexión**
La cuadrícula dinámica lo ayuda a colocar nuevas formas vertical y horizontalmente en relación con las formas que ya ha colocado en el dibujo. Respecto a los puntos de conexión, una vez marcados como marcados, nos servirá para ver los puntos de conexión cuando estemos en proceso de conectarnos a ellos. Podemos lograr ambas opciones usando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Soporte de Redes Dinámicas y Puntos de Conexión en los Planos Visio**
 los[Ventana](http://www.aspose.com/api/net/diagram/aspose.diagram/window) La clase ofrece propiedades DynamicGridEnabled y ShowConnectionPoints. Estas propiedades se pueden usar para aplicar configuraciones para admitir cuadrículas dinámicas y mostrar opciones de puntos de conexión.
#### **Agregar muestra de programación de soporte**
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
## **Mostrar y ocultar cuadrículas, reglas, guías y saltos de página del Visio Diagram**
 Microsoft Office Visio tiene un par de reglas, una cuadrícula y dos tipos de guías y una bandera de saltos de página para ver qué se imprimirá en cada página. Los desarrolladores pueden aplicar esta configuración usando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/)La configuración se aplica globalmente a una sola página.

 los[Ventana](http://www.aspose.com/api/net/diagram/aspose.diagram/window)La clase ofrece las propiedades ShowGrid, ShowGuides, ShowRulers y ShowPageBreaks. Estas propiedades se pueden usar para aplicar configuraciones para mostrar y ocultar cuadrículas, guías, reglas y saltos de página.
### **Ejemplo de programación**
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
