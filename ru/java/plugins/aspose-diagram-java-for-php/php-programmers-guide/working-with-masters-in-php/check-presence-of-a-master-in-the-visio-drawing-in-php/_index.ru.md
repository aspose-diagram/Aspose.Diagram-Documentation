---
title: Проверить наличие мастера в чертеже Visio в PHP
type: docs
weight: 10
url: /ru/java/check-presence-of-a-master-in-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Проверка присутствия Мастера по ID**
 Чтобы проверить присутствие мастера по идентификатору, используя**Aspose.Diagram Java для PHP** , вызов**check_presence_master_by_id** метод**CheckPresenceOfMaster** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 public static function check_presence_master_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$master_id = 2;

\# check master by id

$is_present = $diagram->getMasters()->isExist($master_id);

print "Master Presence : ".(string)$is_present.PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Проверка присутствия мастера по имени**
 Чтобы проверить присутствие мастера по имени, используя**Aspose.Diagram Java для PHP** , вызов**check_presence_master_by_name** метод**CheckPresenceOfMaster** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 public static function check_presence_master_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Set master name

$master_name = "Background tranquil .2";

\# check master object by name

$is_present = $diagram->getMasters()->isExist($master_name);

print "Master Presence : ".(string)$is_present.PHP_EOL;

}

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Проверить наличие мастера в чертеже Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/CheckPresenceOfMaster.php)
