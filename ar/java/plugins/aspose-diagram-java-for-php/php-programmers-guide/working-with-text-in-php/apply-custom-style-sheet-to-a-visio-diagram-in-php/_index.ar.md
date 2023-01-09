---
title: تطبيق ورقة أنماط مخصصة على Visio Diagram في PHP
type: docs
weight: 10
url: /ar/java/apply-custom-style-sheet-to-a-visio-diagram-in-php/
---
## **Aspose.Diagram - تطبيق ورقة الأنماط المخصصة على Visio Diagram**
 لتطبيق ورقة أنماط مخصصة على Visio Diagram باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**ApplyCustomStyleSheet** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes =$diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i<(int)(string)$shapes->getCount()) {

$shape=$shapes->get($i);

if($shape->getNameU()=="Process") {

$source_shape =$shape;

break;

}

$i+= 1;

}

\# Find the required style sheet

$stylesheets=$diagram->getStyleSheets();

$j=0;

while($j<(int)(string)$stylesheets->getCount()) {

$stylesheet=$stylesheets->get($j);

if($stylesheet->getName() == "Basic") {

$custom_stylesheet = $stylesheet;

break;

}

$j+= 1;

}

if ($source_shape!=null && $custom_stylesheet !=null) {

\# Apply text style

$source_shape->setTextStyle($custom_stylesheet);

\# Apply fill style

$source_shape->setFillStyle($custom_stylesheet);

\# Apply line style

$source_shape->setLineStyle($custom_stylesheet);

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ApplyCustomStyleSheet.vdx", $saveFileFormat->VDX);

print "Applied custom stylesheet to a visio diagram.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تطبيق ورقة أنماط مخصصة على Visio Diagram (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithText/ApplyCustomStyleSheet.php)
