---
title: Удалить все макросы из Visio Diagram в Ruby
type: docs
weight: 50
url: /ru/java/remove-all-macros-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Удалить все макросы из Visio Diagram**
 Чтобы удалить все макросы из Visio Diagram с помощью**Aspose.Diagram Java для рубина** , просто вызовите**RemoveAllMacrosFromDiagram** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# remove all macros

diagram.setVbProjectData(nil)

\# Save as VDX

diagram.save(data_dir + "RemoveAllMacros.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Removed all macros from diagram successfully!"

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Удалить все макросы из папки Visio Diagram (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/removeallmacrosfromdiagram.rb)
