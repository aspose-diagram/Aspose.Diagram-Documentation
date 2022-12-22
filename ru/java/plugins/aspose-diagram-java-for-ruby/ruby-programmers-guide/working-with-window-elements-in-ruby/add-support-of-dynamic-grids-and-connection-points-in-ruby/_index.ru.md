---
title: Добавить поддержку динамических сеток и точек подключения в Ruby
type: docs
weight: 10
url: /ru/java/add-support-of-dynamic-grids-and-connection-points-in-ruby/
---
## **Aspose.Diagram — Добавлена поддержка динамических сеток и точек подключения**
 Чтобы добавить поддержку динамических сеток и точек соединения с помощью**Aspose.Diagram Java для рубина** , просто вызовите**Адддинамикгридсандконнектионпойнтс** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# get window object by index

window = diagram.getWindows().get(0)

\# check dynamic grid option

window.setDynamicGridEnabled(1)

\# check connection points option

window.setShowConnectionPoints(1)

\# Save as VDX

diagram.save(data_dir + "AddDynamicGridsAndConnectionPoints.vsx", Rjb::import('com.aspose.diagram.SaveFileFormat').VSX)

puts "Added Support of Dynamic Grids and Connection Points in the Visio Drawings."

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Добавить поддержку динамических сеток и точек подключения (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/adddynamicgridsandconnectionpoints.rb)
