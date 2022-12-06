---
title: Добавить комментарии к Visio Рисунки в PHP
type: docs
weight: 10
url: /ru/java/add-comments-to-visio-drawings-in-php/
---
## **Aspose.Diagram - Добавить комментарии к чертежам Visio**
 Для добавления комментариев к чертежам Visio с помощью**Aspose.Diagram Java для PHP** , просто вызовите**Добавить комментарий к диаграмме** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Add comment

$diagram->getPages()->getPage(0)->addComment(7.205905511811023, 3.880708661417323, "test@");

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddComment.vdx", $saveFileFormat->VDX);

print "Added comment successfully!".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Добавить комментарии к Visio Чертежи (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/AddCommentToDiagram.php)
