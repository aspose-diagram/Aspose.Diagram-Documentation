---
title: Trabajar con elementos de ventana
type: docs
weight: 130
url: /es/java/working-with-window-elements/
---
## **Recuperar elementos de ventana del dibujo Visio**
 La ventana principal de la aplicación Visio puede contener cualquier archivo Visio abierto, al igual que los navegadores web modernos permiten múltiples páginas web con pestañas en una ventana. Los desarrolladores pueden recuperar objetos de Windows usando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 los[VentanaColección](https://reference.aspose.com/diagram/java/com.aspose.diagram/windowcollection) objeto representa una lista de[Ventana](https://reference.aspose.com/diagram/java/com.aspose.diagram/window)objetos disponibles en el dibujo. La propiedad Windows, expuesta por la clase Diagram, admite una colección de objetos Aspose.Diagram.Window. Esta propiedad se puede utilizar para recuperar la información de la ventana, es decir, el ID de la ventana, el tipo, la altura, el ancho y el estado.

**Una ventana de consola que muestra la salida del código.**

![todo:imagen_alternativa_texto](http://i.imgur.com/zduARGh.png)
### **Recuperar muestra de programación de elementos de ventana**

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

## **Agregar elemento de ventana al Visio Diagram**
 La ventana principal de la aplicación Visio puede contener cualquier archivo Visio abierto, al igual que los navegadores web modernos permiten múltiples páginas web con pestañas en una ventana. Los desarrolladores ahora pueden agregar un nuevo objeto de ventana en una instancia Microsoft Visio usando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

El objeto Ventana representa una ventana abierta en una instancia Microsoft Visio. El método Add, expuesto por la clase WindowCollection, permite agregar un nuevo objeto Ventana.
### **Agregar muestra de programación de elemento de ventana**

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

## **Agregar soporte de cuadrículas dinámicas y puntos de conexión**
La cuadrícula dinámica lo ayuda a colocar nuevas formas vertical y horizontalmente en relación con las formas que ya ha colocado en el dibujo. Respecto a los puntos de conexión, una vez marcados como marcados, nos servirá para ver los puntos de conexión cuando estemos en proceso de conectarnos a ellos. Podemos lograr ambas opciones usando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).
### **Soporte de Redes Dinámicas y Puntos de Conexión en los Planos Visio**
La clase Window ofrece propiedades DynamicGridEnabled y ShowConnectionPoints. Estas propiedades se pueden usar para aplicar configuraciones para admitir cuadrículas dinámicas y mostrar opciones de puntos de conexión.

**Una aplicación Visio que muestra las opciones en Visio.**

![todo:imagen_alternativa_texto](http://i.imgur.com/bxsJIwF.png)
#### **Agregar muestra de programación de soporte**

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

## **Mostrar y ocultar cuadrículas, reglas, guías y saltos de página del Visio Diagram**
 Microsoft Office Visio tiene un par de reglas, una cuadrícula y dos tipos de guías y una bandera de saltos de página para ver qué se imprimirá en cada página. Los desarrolladores pueden aplicar esta configuración usando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)La configuración se aplica globalmente a una sola página.

La clase Window ofrece las propiedades ShowGrid, ShowGuides, ShowRulers y ShowPageBreaks. Estas propiedades se pueden usar para aplicar configuraciones para mostrar y ocultar cuadrículas, guías, reglas y saltos de página.

**Una aplicación Visio que muestra las opciones en Visio.**

![todo:imagen_alternativa_texto](http://i.imgur.com/E0pvXbP.png)
### **Ejemplo de programación**

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

