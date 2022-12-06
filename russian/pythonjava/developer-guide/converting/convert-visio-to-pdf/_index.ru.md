---
title:  Конвертировать Visio в формат PDF
linktitle: Конвертировать Visio в PDF
type: docs
weight: 10
url: /ru/python-java/convert-visio-to-pdf/
description: This topic show you how to convert Visio to PDF formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PDF with a few lines of code.
---
## **Экспорт в PDF**
{{% alert color="primary" %}}

Aspose.Diagram для Python через Java непосредственно записывает информацию о API и номере версии в выходных документах. Например, при рендеринге чертежа в PDF Aspose.Diagram for Java заполняется**Заявление**поле со значением «Aspose.Diagram» и**PDF-продюсер**поле со значением, например «Aspose.Diagram 17,9».

Обратите внимание, что вы не можете поручить Aspose.Diagram для Python через Java изменить или удалить эту информацию из выходных документов.

{{% /alert %}}

В этой статье объясняется, как экспортировать Microsoft Visio diagram в PDF, используя Aspose.Diagram для Python через Java.

Используйте конструктор класса Diagram для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения.

[VSD diagram](ExportToPDF.vsd) является примером файла чертежа для экспорта в PDF. Вы также можете использовать другие форматы diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX или VSX).

Чтобы экспортировать VSD diagram в PDF:

1. Создайте экземпляр класса Diagram.
1. Вызовите метод сохранения классов Diagram и установите выходной формат PDF.

### **Экспорт в PDF Образец программирования**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToPDF.py" >}}

### **Разделить несколько страниц**
Aspose.Diagram for Java позволяет разделить несколько страниц при преобразовании Microsoft Visio Diagram в PDF. В следующем фрагменте кода показана функциональность.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.py" >}}
