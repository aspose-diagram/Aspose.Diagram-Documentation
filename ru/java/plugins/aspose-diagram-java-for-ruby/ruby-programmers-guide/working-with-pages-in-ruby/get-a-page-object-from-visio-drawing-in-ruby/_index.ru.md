---
title: Получить объект страницы из Visio Рисование в Ruby
type: docs
weight: 10
url: /ru/java/get-a-page-object-from-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Получение объекта страницы по идентификатору**
 Чтобы получить объект страницы по идентификатору, используя**Aspose.Diagram Java для рубина** , вызов**get_page_object_by_id** метод**GetPageObject** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 def get_page_object_by_id() 

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    page_id = 0

    # Get page object by id

    page = diagram.getPages().getPage(page_id)

    puts "Page : " + page.to_string

end

{{< /highlight >}}
## **Aspose.Diagram - Получение объекта страницы по имени**
 Чтобы получить объект страницы по имени, используя**Aspose.Diagram Java для рубина** , вызов**get_page_object_by_name** метод**GetPageObject** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 def get_page_object_by_name() 

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Set page name

    page_name = "Flow 1"

    # Get page object by name

    page = diagram.getPages().getPage(page_name)

    puts "Page : " + page.to_string

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить объект страницы из чертежа Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageobject.rb)
