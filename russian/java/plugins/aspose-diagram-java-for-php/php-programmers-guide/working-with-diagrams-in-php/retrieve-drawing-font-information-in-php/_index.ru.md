---
title: Получить информацию о шрифте чертежа в PHP
type: docs
weight: 40
url: /ru/java/retrieve-drawing-font-information-in-php/
---
## **Aspose.Diagram - Получить информацию о шрифте чертежа**
 Чтобы получить информацию о шрифте чертежа с помощью**Aspose.Diagram Java для PHP** , просто вызовите**GetDiagramFontInfo** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

$fonts = $diagram->getFonts();

$i = 0;

while ($i<sizeof($fonts->getCount())) {

$font = $fonts->get($i);

\# Display information about the fonts

print $font->getName();

$i+=1;

}

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить информацию о шрифте чертежа (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetDiagramFontInfo.php)
