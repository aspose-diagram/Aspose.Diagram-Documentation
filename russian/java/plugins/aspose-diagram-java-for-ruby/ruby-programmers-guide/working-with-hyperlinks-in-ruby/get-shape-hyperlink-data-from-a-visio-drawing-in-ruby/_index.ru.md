---
title: Получить данные гиперссылки формы из чертежа Visio в Ruby
type: docs
weight: 20
url: /ru/java/get-shape-hyperlink-data-from-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram — Получить данные гиперссылки формы**
Чтобы получить данные гиперссылки формы, используя**Aspose.Diagram Java для рубина** , просто вызовите**GetShapeHyperlinkData** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Hyperlinks.vdx")

\# Получить определенную форму

shape = diagram.getPages().getPage("Поток 1").getShapes().getShape(1)

гиперссылки = shape.getHyperlinks()

я = 0

 в то время как я< hyperlinks.getCount()

    hyperlink = hyperlinks.get(i)

    puts "Address: " + hyperlink.getAddress().getValue().to_s

    puts "Sub Address: " + hyperlink.getSubAddress().getValue().to_s

    puts "Description: " + hyperlink.getDescription().getValue().to_s

    i +=1

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получение данных гиперссылки формы из чертежа Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/getshapehyperlinkdata.rb)
