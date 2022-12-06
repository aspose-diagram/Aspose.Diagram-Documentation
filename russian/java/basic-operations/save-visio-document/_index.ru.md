---
title: Сохранить документ Visio программно
linktitle: Сохранить документ Visio
type: docs
weight: 30
url: /ru/java/save-visio-document/
description: На этой странице описывается, как сохранить документ Visio в файл, поток с библиотекой Aspose.Diagram.
---
## **Visio Обзор сохранения чертежа**
 Использовать[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\) метод сохранения чертежа Microsoft Visio. Есть перегрузки, позволяющие сохранить рисунок в файл. Чертеж можно сохранить в любом формате сохранения, поддерживаемом Aspose.Diagram. Список всех поддерживаемых форматов сохранения см.[СохранитьФайлФормат](https://reference.aspose.com/diagram/java/com.aspose.diagram/SaveFileFormat) перечисление.
## **Сохранение Visio Diagram**
 Класс Diagram класса Aspose.Diagram API представляет чертеж Visio, и разработчики могут сохранять его объект Visio diagram в любом поддерживаемом формате файла. Чтобы сохранить файл Microsoft Visio, просто используйте[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) он принимает имя файла с полным путем или объект файлового потока. Aspose.Diagram API выводит формат сохранения из расширения файла, а также предлагает дополнительный параметр SaveFileFormat для указания формата выходного файла.
### **Сохраните Visio Diagram в любом поддерживаемом формате файла**
Используя Aspose.Diagram API, разработчики могут сохранить Visio diagram в любом поддерживаемом формате файла, как указано ниже:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG и XAML**
### **Сохранение Diagram Пример программирования**
В приведенном ниже примере документ сохраняется в файл.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-SaveVisioDiagram-SaveVisioDiagram.java" >}}
## **Указание Visio параметров сохранения**
 Есть несколько[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) перегрузки методов, которые принимают объект SaveOptions. Это должен быть объект класса, производного от класса SaveOptions. У каждого формата сохранения есть соответствующий класс, который содержит параметры сохранения для этого формата сохранения, например, есть PdfSaveOptions для формата сохранения SaveFileFormat.PDF.
### **Visio Diagram Параметры сохранения**
Эти примеры показывают, как:

- [Используйте параметры сохранения Diagram](/diagram/ru/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Используйте параметры сохранения PDF](/diagram/ru/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Используйте параметры сохранения HTML](/diagram/ru/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Используйте параметры сохранения изображения](/diagram/ru/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Используйте параметры сохранения SVG](/diagram/ru/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
#### **Использование параметров сохранения Diagram**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.java" >}}



#### **Использование параметров сохранения PDF**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате PDF.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.java" >}}



#### **Использование параметров сохранения HTML**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате HTML.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.java" >}}



#### **Использование параметров сохранения изображения**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате изображения.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.java" >}}
#### **Использование параметров сохранения SVG**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формате SVG.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.java" >}}
