---
title: Establecer propiedades de forma de hito en PHP
type: docs
weight: 110
url: /es/java/set-milestone-shape-properties-in-php/
---
## **Aspose.Diagram - Establecer propiedades de forma de hito**
 Para establecer las propiedades de la forma de un hito mediante**Aspose.Diagram Java para PHP** , simplemente invocar**EstablecerHitoFormaPropiedades** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shape_id=1;

\# Get timeline shape

$milestone=$diagram->getPages()->getPage("Flow 1")->getShapes()->getShape($shape_id);

\# Initialize MilestoneHelper object

$milestone_helper = new MilestoneHelper($milestone);

\# Set date format

$milestone_helper->setDateFormat(21);

\# Set auto update flag

$milestone_helper->setAutoUpdate(true);

\# Set milestone type

$milestone_helper->setType(6);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetMilestoneShapeProperties.vdx", $saveFileFormat->VDX);

print "Set milestone shape properties.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Establecer propiedades de forma de hito (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetMilestoneShapeProperties.php)
