---
title: PHP'de Kilometre Taşı Şekli Özelliklerini Ayarlama
type: docs
weight: 110
url: /tr/java/set-milestone-shape-properties-in-php/
---
## **Aspose.Diagram - Kilometre Taşı Şekli Özelliklerini Ayarla**
 Kilometre Taşı Şekli Özelliklerini Ayarlamak için**PHP için Aspose.Diagram Java** , sadece çağırmak**SetMilestoneShapeProperties** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

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
## **Çalışan Kodu İndir**
 İndirmek**Kilometre Taşı Şekli Özelliklerini Ayarla (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetMilestoneShapeProperties.php)
