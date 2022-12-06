---
title: Получить информацию о соединителях Visio в Ruby
type: docs
weight: 20
url: /ru/java/retrieve-visio-connectors-information-in-ruby/
---
## **Aspose.Diagram - Получить информацию о разъемах Visio**
 Чтобы получить информацию о соединителях Visio с помощью**Aspose.Diagram Java для рубина** , просто вызовите**GetConnectorsInfo** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 данные_dir = File.dirname(File.dirname(File.dirname(File.dirname(__ФАЙЛ__)))) + '/данные/'

\# Создать экземпляр Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

коннекторы = diagram.getPages().getPage(0).getConnects()

я = 0

 в то время как я< connectors.getCount()

    connector = connectors.get(i)

    # Display information about the Connectors

    puts "From Shape ID : " + connector.getFromSheet().to_s

    puts "To Shape ID : " + connector.getToSheet().to_s

    i +=1

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить информацию о разъемах Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getconnectorsinfo.rb)

