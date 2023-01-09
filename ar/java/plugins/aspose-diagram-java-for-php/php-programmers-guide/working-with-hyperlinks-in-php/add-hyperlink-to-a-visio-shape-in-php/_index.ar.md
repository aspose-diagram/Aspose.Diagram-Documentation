---
title: أضف ارتباطًا تشعبيًا إلى شكل Visio في PHP
type: docs
weight: 10
url: /ar/java/add-hyperlink-to-a-visio-shape-in-php/
---
## **Aspose.Diagram - إضافة ارتباط تشعبي**
 لإضافة ارتباط تشعبي باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**إضافة ارتباط تشعبي إلى شكل** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "Drawing.vsd");

\# Initialize Hyperlink object

$hyperlink = new Hyperlink();

\# Set address value

$hyperlink->getAddress()->setValue("http://www.google.com/");

\# Set sub address value

$hyperlink->getSubAddress()->setValue("Sub address here");

\# Set description value

$hyperlink->getDescription()->setValue("Description here");

\# Set name

$hyperlink->setName("MyHyperLink");

\# Add hyperlink to the shape

$diagram->getPages()->getPage("Flow 1")->getShapes()->getShape(1)->getHyperlinks()->add($hyperlink);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir . "Hyperlinks.vdx", $saveFileFormat->VDX);

print "Added hyperlik to shape successfully!".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**إضافة ارتباط تشعبي إلى شكل Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHyperlinks/AddHyperlinkToShape.php)
