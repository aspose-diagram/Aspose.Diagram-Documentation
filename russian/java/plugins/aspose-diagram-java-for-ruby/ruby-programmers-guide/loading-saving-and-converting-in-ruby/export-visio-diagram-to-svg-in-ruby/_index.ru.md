---
title: Экспорт Visio Diagram в SVG в Ruby
type: docs
weight: 50
url: /ru/java/export-visio-diagram-to-svg-in-ruby/
---
## **Aspose.Diagram - Экспорт Visio Diagram в SVG**
 Чтобы экспортировать Visio Diagram в SVG, используя**Aspose.Diagram Java для рубина** , просто вызовите**ЭкспорттоСвг** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as SVG

diagram.save(data_dir + "Diagram.svg", Rjb::import('com.aspose.diagram.SaveFileFormat').SVG)

puts "Exported visio diagram to SVG."

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Экспорт Visio Diagram в SVG (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttosvg.rb)
