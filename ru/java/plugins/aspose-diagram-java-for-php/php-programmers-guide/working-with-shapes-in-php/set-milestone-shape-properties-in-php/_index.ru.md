---
title: Установить свойства формы вехи в PHP
type: docs
weight: 110
url: /ru/java/set-milestone-shape-properties-in-php/
---
## **Aspose.Diagram - Установить свойства формы вехи**
 Чтобы задать свойства формы вехи, используя**Aspose.Diagram Java для PHP** , просто вызовите**SetMilestoneShapeProperties** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

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
## **Скачать рабочий код**
 Скачать**Задать свойства формы вехи (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetMilestoneShapeProperties.php)
