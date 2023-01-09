---
title: Защита и снятие защиты диаграмм в PHP
type: docs
weight: 20
url: /ru/java/protect-and-unprotect-diagrams-in-php/
---
## **Aspose.Diagram - Диаграммы защиты и снятия защиты**
 Чтобы защитить и снять защиту диаграмм с помощью**Aspose.Diagram Java для PHP** , просто вызовите**ЗащититьСнять защитуДиаграмма** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "drawing.vsd");

$diagram->getDocumentSettings()->setProtectBkgnds(1);

$diagram->getDocumentSettings()->setProtectMasters(1);

$diagram->getDocumentSettings()->setProtectShapes(1);

$diagram->getDocumentSettings()->setProtectStyles(1);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir . "ProtectUnprotectDiagram.vdx", $saveFileFormat->VDX);

print "Applied protection on diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Защита и снятие защиты диаграмм (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithProtection/ProtectUnprotectDiagram.php)
