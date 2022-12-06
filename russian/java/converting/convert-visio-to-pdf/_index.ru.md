---
title:  Конвертировать Visio в формат PDF
linktitle: Конвертировать Visio в PDF
type: docs
weight: 10
url: /ru/java/convert-visio-to-pdf/
description: В этом разделе показано, как Aspose.Diagram позволяет конвертировать Visio в форматы PDF. Конвертируйте VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM в PDF с помощью нескольких строк кода.
---
## **Экспорт в PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Java непосредственно записывает информацию о API и номере версии в выходных документах. Например, при преобразовании чертежа в PDF Aspose.Diagram for Java заполняется**Заявление**поле со значением «Aspose.Diagram» и**PDF-продюсер**поле со значением, например «Aspose.Diagram 17,9».

Обратите внимание, что вы не можете поручить Aspose.Diagram for Java API изменить или удалить эту информацию из выходных документов.

{{% /alert %}}

 В этой статье объясняется, как экспортировать Microsoft Visio diagram в PDF, используя[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Использовать[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

На изображении ниже показан код VSD diagram, который фрагменты кода ниже экспортируют в PDF. Вы также можете использовать другие форматы diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX или VSX).

**Исходный файл.**

![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_1.png)

Чтобы экспортировать VSD diagram в PDF:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод сохранения классов Diagram и установите выходной формат PDF.

Ниже приведено изображение выходного PDF-файла.

**Выходной PDF-файл.**

![дело:изображение_альтернативный_текст](how-to-convert-a-visio-diagram_2.png)
### **Экспорт в PDF Образец программирования**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToPDF-ExportToPDF.java" >}}
### **Разделить несколько страниц**
Aspose.Diagram for Java позволяет разделить несколько страниц при преобразовании Microsoft Visio Diagram в PDF. В следующем фрагменте кода показана функциональность.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.java" >}}
### **Использовать обратный вызов для сохранения страницы**
Если у вас несколько страниц, Aspose.Diagram for Java позволяет использовать обратный вызов для сохранения страницы при преобразовании Microsoft Visio Diagram в PDF. В следующем фрагменте кода показана функциональность.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-1.java" >}}

#### **Класс TestDiagramPageSavingCallback**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-2.java" >}}
