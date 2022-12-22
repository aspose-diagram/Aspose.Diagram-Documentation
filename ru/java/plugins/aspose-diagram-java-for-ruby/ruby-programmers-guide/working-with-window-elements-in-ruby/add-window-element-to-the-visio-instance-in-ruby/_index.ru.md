---
title: Добавьте элемент окна в экземпляр Visio в Ruby
type: docs
weight: 20
url: /ru/java/add-window-element-to-the-visio-instance-in-ruby/
---
## **Aspose.Diagram — добавить элемент окна в экземпляр Visio**
 Чтобы добавить элемент окна в экземпляр Visio, используя**Aspose.Diagram Java для рубина** , просто вызовите**Аддвиндоэлемент** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# initialize window object

window = Rjb::import('com.aspose.diagram.Window').new

\# set window state

window.setWindowState(Rjb::import('com.aspose.diagram.WindowStateValue').MAXIMIZED)

\# set window height

window.setWindowHeight(500)

\# set window width

window.setWindowWidth(500)

\# set window type

window.setWindowType(Rjb::import('com.aspose.diagram.WindowTypeValue').STENCIL)

\# add window object

diagram.getWindows().add(window)

\# save in any supported format

diagram.save(data_dir + "AddWindowElement.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added window element to the visio instance."

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Добавить элемент окна в экземпляр Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/addwindowelement.rb)
