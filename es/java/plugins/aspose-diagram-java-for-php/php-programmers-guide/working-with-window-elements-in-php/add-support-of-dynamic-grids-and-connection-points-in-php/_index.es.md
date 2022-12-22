---
title: Agregar soporte de cuadrículas dinámicas y puntos de conexión en PHP
type: docs
weight: 10
url: /es/java/add-support-of-dynamic-grids-and-connection-points-in-php/
---
## **Aspose.Diagram - Agregar compatibilidad con cuadrículas dinámicas y puntos de conexión**
 Para agregar compatibilidad con cuadrículas dinámicas y puntos de conexión mediante**Aspose.Diagram Java para PHP** , simplemente invocar**AddDynamicGridsAndConnectionPoints** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# get window object by index

$window=$diagram->getWindows()->get(0);

\# check dynamic grid option

$window->setDynamicGridEnabled(1);

\# check connection points option

$window->setShowConnectionPoints(1);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddDynamicGridsAndConnectionPoints.vsx", $saveFileFormat->VSX);

print "Added Support of Dynamic Grids and Connection Points in the Visio Drawings.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Agregar soporte de cuadrículas dinámicas y puntos de conexión (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddDynamicGridsAndConnectionPoints.php)
