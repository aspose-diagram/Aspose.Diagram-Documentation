---
title: Получить все слои из Visio Diagram в Ruby
type: docs
weight: 30
url: /ru/java/retrieve-all-layers-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram — Получить все слои**
 Чтобы получить все слои с помощью**Aspose.Diagram Java для рубина** , просто вызовите**GetAllLayers** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# получить страницу Visio

страница = diagram.getPages().getPage(0)

слои = страница.getPageSheet().getLayers()

я = 0

 в то время как я< layers.getCount()

    layer = layers.get(i)

    puts "Name: " + layer.getName().getValue().to_s

    puts "Visibility: " + layer.getVisible().getValue().to_s

    puts "Status: " + layer.getStatus().getValue().to_s



    i +=1

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить все слои из Visio Diagram (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/getalllayers.rb)
