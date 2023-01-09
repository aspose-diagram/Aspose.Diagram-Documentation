---
title: Добавить поддержку динамических сеток и точек подключения в PHP
type: docs
weight: 10
url: /ru/java/add-support-of-dynamic-grids-and-connection-points-in-php/
---
## **Aspose.Diagram — Добавлена поддержка динамических сеток и точек подключения**
 Чтобы добавить поддержку динамических сеток и точек соединения с помощью**Aspose.Diagram Java для PHP** , просто вызовите**Адддинамикгридсандконнектионпойнтс** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# get window object by index

$window=$diagram->getWindows()->get(0);

\# check dynamic grid option

$window->setDynamicGridEnabled(1);

\# check connection points option

$window->setShowConnectionPoints(1);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddDynamicGridsAndConnectionPoints.vsx", $saveFileFormat->VSX);

print "Added Support of Dynamic Grids and Connection Points in the Visio Drawings.".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Добавить поддержку динамических сеток и точек подключения (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddDynamicGridsAndConnectionPoints.php)
