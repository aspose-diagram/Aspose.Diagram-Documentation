---
title: Получить главный объект из чертежа в PHP
type: docs
weight: 20
url: /ru/java/get-master-object-from-drawing-in-php/
---
## **Aspose.Diagram - Получение Мастер-объекта по ID**
 Чтобы получить мастер-объект по идентификатору, используя**Aspose.Diagram Java для PHP** , вызов**get_master_object_by_id** метод**ПолучитьМастерОбъект** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 public static function get_master_object_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$master_id = 2;

\# Get master object by id

$master = $diagram->getMasters()->getMaster($master_id);

print "Master ID : ".(string)$master->getID().PHP_EOL;

print "Master Name : ".(string)$master->getName().PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Получение главного объекта по имени**
 Чтобы получить главный объект по имени, используя**Aspose.Diagram Java для PHP** , вызов**get_master_object_by_name** метод**ПолучитьМастерОбъект** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 public static function get_master_object_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Set master name

$master_name = "Background tranquil .2";

\# Get master object by name

$master = $diagram->getMasters()->getMasterByName($master_name);

print "Master ID : ".(string)$master->getID().PHP_EOL;

print "Master Name : ".(string)$master->getName().PHP_EOL;

}

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить основной объект из чертежа (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterObject.php)
