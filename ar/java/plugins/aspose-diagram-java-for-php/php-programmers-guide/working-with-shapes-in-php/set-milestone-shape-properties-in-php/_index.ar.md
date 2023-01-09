---
title: قم بتعيين خصائص الشكل الرئيسي في PHP
type: docs
weight: 110
url: /ar/java/set-milestone-shape-properties-in-php/
---
## **Aspose.Diagram - تعيين خصائص الشكل الرئيسي**
 لتعيين خصائص الشكل الرئيسي باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**SetMilestoneShapeProperties** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

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
## **قم بتنزيل كود التشغيل**
 تحميل**تعيين خصائص الشكل الرئيسي (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetMilestoneShapeProperties.php)
