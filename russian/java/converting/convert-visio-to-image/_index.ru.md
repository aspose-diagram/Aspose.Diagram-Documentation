---
title:  Конвертировать Visio в форматы изображений
linktitle: Преобразовать Visio в изображения
type: docs
weight: 20
url: /ru/java/convert-visio-to-image/
description: В этом разделе показано, как Aspose.Diagram позволяет конвертировать Visio в различные форматы изображений. Конвертируйте Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM в изображения PNG, JPEG, BMP с помощью нескольких строк кода.
---
## **Экспорт диаграмм в форматы файлов изображений**
 В этой статье объясняется, как экспортировать Microsoft Visio diagram в изображение с помощью[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Использовать[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)class' для чтения файлов diagram и метод Save для экспорта diagram в любой поддерживаемый формат изображения. На изображении ниже показан файл VSD, который нужно сохранить в формате PNG. Вы также можете использовать другие форматы diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX или VSX).
**Исходный файл. Обратите внимание, что метки «Стрелка» и «Треугольник» выделены жирным шрифтом.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/WOV36ek.png)

Чтобы экспортировать diagram в изображение:

- Создайте экземпляр класса Diagram.
- Вызовите метод Save класса Diagram и установите формат изображения, в который вы хотите экспортировать. Выходной файл изображения выглядит как исходный файл.

**Выходной файл PNG.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/WOV36ek.png)
### **Пример программирования экспорта в файл изображения**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToImage-ExportToImage.java" >}}

Также можно сохранить в изображение определенную страницу, а не весь документ:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportPageToImage-ExportPageToImage.java" >}}