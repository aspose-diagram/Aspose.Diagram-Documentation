---
title: Работа с изображениями
type: docs
weight: 60
url: /ru/net/working-with-images/
description: В этом разделе объясняется, как вставить или получить изображение со страницы visio с помощью Aspose.Diagram.
---
## **Извлечь все изображения со страницы Visio**
В Microsoft Visio страницы являются либо передним планом, либо фоновыми страницами. Вы можете извлечь изображения с определенной страницы файла Visio.
### **Извлечь изображения**
Объект Page Class представляет область рисования страницы переднего плана или страницы фона. Свойство Shapes, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Shape. Это свойство можно использовать для извлечения всех изображений с определенной страницы.
#### **Пример программирования извлечения изображений**
Следующий фрагмент кода извлекает все изображения с определенной страницы Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ExtractAllImagesFromPage-ExtractAllImagesFromPage.cs" >}}
## **Получить иконки различных форм Visio**
Aspose.Diagram for .NET API теперь позволяет разработчикам получать иконки различных Visio форм.
### **Получение значка формы**
Код в приведенных ниже примерах показывает, как:

1. Загрузите существующий diagram или шаблон.
1. Получить мастер по его индексу
1. Получить главный значок.
1. Сохранить значок в локальном пространстве.
#### **Получить пример программирования значков**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-GetShapeIcon-GetShapeIcon.cs" >}}
## **Замените форму изображения Visio Diagram**
Aspose.Diagram for .NET API позволяет разработчикам получать доступ и заменять доступные формы изображений в файле Visio diagram.
### **Замена формы изображения**
Код в приведенных ниже примерах показывает, как:

1. Загрузите существующий diagram.
1. Повторите выборочные формы страниц.
1. Примените фильтр, чтобы получить формы изображения.
1. Сохраните результат Visio diagram в локальном пространстве.
#### **Замена примера программирования формы изображения**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ReplaceShapePicture-ReplaceShapePicture.cs" >}}
## **Импортировать растровое изображение как форму Visio**
Aspose.Diagram for .NET API теперь позволяет разработчикам импортировать растровое изображение в виде формы.
### **Вставьте изображение BMP в Visio**
Код в приведенных ниже примерах показывает, как:

1. Создайте номер diagram.
1. Получить страницу Visio
1. Импорт растрового изображения в виде фигуры Visio
1. Сохраните номер diagram.
#### **Вставьте образец программирования изображения BMP**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-InsertImageInVisio-InsertImageInVisio.cs" >}}
## **Преобразование указанной области страницы Visio в изображение**
С помощью Aspose.Diagram for .NET API разработчики могут определить область с координатами XY, шириной и высотой, а затем преобразовать эту область в поддерживаемый формат изображения.
### **Преобразование области рисования Visio в изображение**
Код в приведенных ниже примерах показывает, как:

1. Загрузите существующий чертеж Visio
1. Определить площадь прямоугольника
1. Преобразование указанной области в изображение

**C#**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

Aspose.Diagram.Saving.ImageSaveOptions Options = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

// specify region with XY coordinates, width and height

Options.Area = new RectangleF(0, 0, 1, 1);

// save into the image format

diagram.Save(@"c:\temp\area.png", Options);

{{< /highlight >}}
