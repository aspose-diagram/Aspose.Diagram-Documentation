---
title: Создайте пустой Visio Diagram в Ruby
type: docs
weight: 10
url: /ru/java/create-an-empty-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Создать пустой Visio Diagram**
 Чтобы создать пустой Visio Diagram с помощью**Aspose.Diagram Java для рубина** , просто вызовите**СоздатьДиаграмму** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new

\# Save as VDX

diagram.save(data_dir + "CreateDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created visio diagram successfully!"

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Создайте пустой Visio Diagram (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/creatediagram.rb)
