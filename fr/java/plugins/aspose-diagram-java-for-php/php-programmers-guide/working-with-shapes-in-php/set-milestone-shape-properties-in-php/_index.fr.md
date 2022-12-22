---
title: Définir les propriétés de forme de jalon en PHP
type: docs
weight: 110
url: /fr/java/set-milestone-shape-properties-in-php/
---
## **Aspose.Diagram - Définir les propriétés de forme de jalon**
 Pour définir les propriétés de forme de jalon à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**SetMilestoneShapePropertiesSetMilestoneShapeProperties** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

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
## **Télécharger le code d'exécution**
 Télécharger**Définir les propriétés de la forme du jalon (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetMilestoneShapeProperties.php)
