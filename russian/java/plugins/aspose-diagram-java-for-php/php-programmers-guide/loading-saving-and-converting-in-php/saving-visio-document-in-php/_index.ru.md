---
title: Сохранение документа Visio в PHP
type: docs
weight: 100
url: /ru/java/saving-visio-document-in-php/
---
## **Aspose.Diagram - Сохранение Visio Документ**
 Чтобы сохранить документ Visio, используя**Aspose.Diagram Java для PHP**, вы можете использовать следующий код.

**PHP-код**

{{< highlight "php" >}}

 # Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram=new Diagram();

$diagram->save($dataDir."Diagram.vdx", $saveFileFormat->VDX);

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Экспорт Visio Diagram в XPS (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/SavingVisioDocument.php)
