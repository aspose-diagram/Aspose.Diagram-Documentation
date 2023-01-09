---
title: Проверка наличия мастера в чертеже Visio в Ruby
type: docs
weight: 10
url: /ru/java/check-presence-of-a-master-in-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Проверка присутствия Мастера по ID**
 Чтобы проверить присутствие мастера по идентификатору, используя**Aspose.Diagram Java для рубина** , вызов**check_presence_master_by_id** метод**CheckPresenceOfMaster** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 def check_presence_master_by_id()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    master_id = 2

    # check master by id

    is_present = diagram.getMasters().isExist(master_id)

    puts "Master Presence : " + is_present.to_s

end

{{< /highlight >}}
## **Aspose.Diagram - Проверка присутствия мастера по имени**
 Чтобы проверить присутствие мастера по имени, используя**Aspose.Diagram Java для рубина** , вызов**check_presence_master_by_name** метод**CheckPresenceOfMaster** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 def check_presence_master_by_name()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Set master name

    master_name = "Background tranquil .2"

    # check master object by name

    is_present = diagram.getMasters().isExist(master_name)

    puts "Master Presence : " + is_present.to_s

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Проверить наличие мастера в чертеже Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/checkpresenceofmaster.rb)
