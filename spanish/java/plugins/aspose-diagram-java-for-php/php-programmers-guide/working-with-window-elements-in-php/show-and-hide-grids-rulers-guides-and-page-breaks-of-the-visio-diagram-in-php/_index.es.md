---
title: Mostrar y ocultar cuadrículas, reglas, guías y saltos de página del Visio Diagram en PHP
type: docs
weight: 40
url: /es/java/show-and-hide-grids-rulers-guides-and-page-breaks-of-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Mostrar y ocultar cuadrículas, reglas, guías y saltos de página del Visio Diagram**
Para mostrar y ocultar cuadrículas, reglas, guías y saltos de página del Visio Diagram usando**Aspose.Diagram Java para PHP** , simplemente invocar**MostrarOcultarPropiedades** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram =new Diagram($dataDir."Drawing.vsd");

\# get window object by index

$window=$diagram->getWindows()->get(0);

\# set visibility of grid

$window->setShowGrid(1);

\# set visibility of guides

$window->setShowGuides(1);

\# set visibility of rulers

$window->setShowRulers(1);

\# set visibility of page breaks

$window->setShowPageBreaks(1);

\# save in any supported format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ShowHideProperties.vdx", $saveFileFormat->VDX);

print "Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Mostrar y ocultar cuadrículas, reglas, guías y saltos de página del Visio Diagram (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/ShowHideProperties.php)
