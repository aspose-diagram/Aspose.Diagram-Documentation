---
title: استرجع عناصر النافذة من رسم Visio في PHP
type: docs
weight: 30
url: /ar/java/retrieve-window-elements-from-the-visio-drawing-in-php/
---
## **Aspose.Diagram - استرجاع عناصر النافذة من رسم Visio**
 لاسترداد عناصر النافذة من رسم Visio باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**GetWindowElements** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$windows=$diagram->getWindows();

$i = 0;

while ($i<(int)(string)$windows->getCount()) {

$window=$windows->get($i);

print "ID: ".(string)$window->getID();

print "Type: ".(string)$window->getWindowType();

print "Window height: ".(string)$window->getWindowHeight();

print "Window width: ".(string)$window->getWindowWidth();

print"Window state: ".(string)$window->getWindowState();

$i+= 1;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرجاع عناصر النافذة من رسم Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/GetWindowElements.php)
