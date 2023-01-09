---
title: Agregar elemento de ventana a la instancia Visio en PHP
type: docs
weight: 20
url: /es/java/add-window-element-to-the-visio-instance-in-php/
---
## **Aspose.Diagram - Agregar elemento de ventana a la instancia Visio**
 Para agregar un elemento de ventana a la instancia Visio mediante**Aspose.Diagram Java para PHP** , simplemente invocar**AgregarElementoDeVentana** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# initialize window object

$window = new Window();

\# set window state

$windowStateValue=new WindowStateValue();

$window->setWindowState($windowStateValue->MAXIMIZED);

\# set window height

$window->setWindowHeight(500);

\# set window width

$window->setWindowWidth(500);

\# set window type

$windowTypeValue=new WindowTypeValue();

$window->setWindowType($windowTypeValue->STENCIL);

\# add window object

$diagram->getWindows()->add($window);

\# save in any supported format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddWindowElement.vdx", $saveFileFormat->VDX);

print "Added window element to the visio instance.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Agregar elemento de ventana a la instancia Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddWindowElement.php)
