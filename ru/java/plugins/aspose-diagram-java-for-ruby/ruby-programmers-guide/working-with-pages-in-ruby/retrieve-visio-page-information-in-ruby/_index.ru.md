---
title: Получить информацию о странице Visio в Ruby
type: docs
weight: 30
url: /ru/java/retrieve-visio-page-information-in-ruby/
---
## **Aspose.Diagram - Получить Visio Информация о странице**
 Чтобы получить информацию о странице Visio с помощью**Aspose.Diagram Java для рубина** , просто вызовите**GetPageInfo** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

# page = diagram.getPages().getPage(page_id)

page = diagram.getPages().getPage(0)

puts "Page ID : " + page.getName().to_s

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить информацию о странице Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageinfo.rb)
