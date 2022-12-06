---
title: Добавить комментарии к Visio Рисунки на Ruby
type: docs
weight: 40
url: /ru/java/add-comments-to-visio-drawings-in-ruby/
---
## **Aspose.Diagram - Добавить комментарии к чертежам Visio**
 Для добавления комментариев к чертежам Visio с помощью**Aspose.Diagram Java для рубина** , просто вызовите**Добавить комментарий к диаграмме** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Add comment

diagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@")

\# Save as VDX

diagram.save(data_dir + "AddComment.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added comment successfully!"

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Добавить комментарии к Visio Чертежи (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/addcommenttodiagram.rb)
