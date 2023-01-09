---
title: أضف عنصر Window إلى مثيل Visio في PHP
type: docs
weight: 20
url: /ar/java/add-window-element-to-the-visio-instance-in-php/
---
## **Aspose.Diagram - إضافة عنصر نافذة إلى مثيل Visio**
 لإضافة عنصر إطار إلى مثيل Visio باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**AddWindowElement** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

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
## **قم بتنزيل كود التشغيل**
 تحميل**إضافة عنصر النافذة إلى المثيل Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddWindowElement.php)
