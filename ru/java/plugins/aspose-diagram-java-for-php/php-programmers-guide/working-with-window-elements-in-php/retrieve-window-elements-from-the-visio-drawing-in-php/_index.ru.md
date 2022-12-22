---
title: Получить элементы окна из чертежа Visio в PHP
type: docs
weight: 30
url: /ru/java/retrieve-window-elements-from-the-visio-drawing-in-php/
---
## **Aspose.Diagram — Извлечение оконных элементов из чертежа Visio**
 Извлечение оконных элементов из чертежа Visio с помощью**Aspose.Diagram Java для PHP** , просто вызовите**GetWindowElements** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

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
## **Скачать рабочий код**
 Скачать**Извлечение оконных элементов из чертежа Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/GetWindowElements.php)
