---
title: Получить мастер-объект из чертежа в Ruby
type: docs
weight: 20
url: /ru/java/get-master-object-from-drawing-in-ruby/
---
## **Aspose.Diagram - Получение Мастер-объекта по ID**
 Чтобы получить мастер-объект по идентификатору, используя**Aspose.Diagram Java для рубина** , вызов**get_master_object_by_id** метод**ПолучитьМастерОбъект** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 def get_master_object_by_id()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    master_id = 2

    # Get master object by id

    master = diagram.getMasters().getMaster(master_id)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

end

{{< /highlight >}}
## **Aspose.Diagram - Получение главного объекта по имени**
 Чтобы получить главный объект по имени, используя**Aspose.Diagram Java для рубина** , вызов**get_master_object_by_name** метод**ПолучитьМастерОбъект** модуль. Здесь вы можете увидеть пример кода.

**Рубиновый код**

{{< highlight "ruby" >}}

 def get_master_object_by_name()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Set master name

    master_name = "Background tranquil .2"

    # Get master object by name

    master = diagram.getMasters().getMasterByName(master_name)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

end

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить основной объект из чертежа (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterobject.rb)
