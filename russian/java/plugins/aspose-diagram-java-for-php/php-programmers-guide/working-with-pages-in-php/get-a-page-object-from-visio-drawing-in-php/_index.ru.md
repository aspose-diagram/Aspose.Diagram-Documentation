---
title: Получить объект страницы из Visio Рисование в PHP
type: docs
weight: 10
url: /ru/java/get-a-page-object-from-visio-drawing-in-php/
---
## **Aspose.Diagram - Получение объекта страницы по идентификатору**
 Чтобы получить объект страницы по идентификатору, используя**Aspose.Diagram Java для PHP** , вызов**get_page_object_by_id** метод**GetPageObject** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 public static function get_page_object_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$page_id = 0;

\# Get page object by id

$page = $diagram->getPages()->getPage($page_id);

print "Page : ".(string)$page.PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Получение объекта страницы по имени**
 Чтобы получить объект страницы по имени, используя**Aspose.Diagram Java для PHP** , вызов**get_page_object_by_name** метод**GetPageObject** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 public static function get_page_object_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Set page name

$page_name = "Flow 1";

\# Get page object by name

$page = $diagram->getPages()->getPage($page_name);

print "Page : ".(string)$page.PHP_EOL;

}

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить объект страницы из чертежа Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageObject.php)
