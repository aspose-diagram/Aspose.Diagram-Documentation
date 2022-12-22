---
title: Выберите вариант перенаправления формы соединителя в Ruby
type: docs
weight: 90
url: /ru/java/select-reroute-option-of-the-connector-shape-in-ruby/
---
## **Aspose.Diagram — выберите вариант перенаправления формы соединителя**
 Чтобы выбрать вариант перенаправления формы соединителя, используя**Aspose.Diagram Java для рубина** , просто вызовите**SelectRerouteOption** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Access a particular page

page = diagram.getPages().getPage("Flow 1")

\# get a particular connector shape

shape = page.getShapes().getShape(1)

\# set reroute option

shape.getLayout().getConFixedCode().setValue(Rjb::import('com.aspose.diagram.ConFixedCodeValue').NEVER_REROUTE)

\# Save diagram

diagram.save(data_dir + "SelectRerouteOption.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Seleted reroute option of the connector shape."

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Выберите вариант перенаправления формы соединителя (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/selectrerouteoption.rb)
