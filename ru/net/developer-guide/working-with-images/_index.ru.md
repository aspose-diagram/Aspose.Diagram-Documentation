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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Load memory stream into bitmap object
            System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);

            // Save bmp here
            bitmap.Save(dataDir + "ExtractAllImages" + shape.ID + "_out.bmp");
        }
    }
}

{{< /highlight >}}

## **Получить иконки различных форм Visio**
Aspose.Diagram for .NET API теперь позволяет разработчикам получать иконки различных Visio форм.
### **Получение значка формы**
Код в приведенных ниже примерах показывает, как:

1. Загрузите существующий diagram или шаблон.
1. Получить мастер по его индексу
1. Получить главный значок.
1. Сохранить значок в локальном пространстве.
#### **Получить пример программирования значков**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load stencil file to a diagram object
Diagram stencil = new Diagram(dataDir + "Timeline.vss");
// Get master
Master master = stencil.Masters.GetMaster(1);

using (System.IO.MemoryStream stream = new System.IO.MemoryStream(master.Icon))
{
    // Load memory stream into bitmap object
    System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);
    // Save as png format
    bitmap.Save(dataDir + "MasterIcon_out.png", System.Drawing.Imaging.ImageFormat.Png);
}

{{< /highlight >}}

## **Замените форму изображения Visio Diagram**
Aspose.Diagram for .NET API позволяет разработчикам получать доступ и заменять доступные формы изображений в файле Visio diagram.
### **Замена формы изображения**
Код в приведенных ниже примерах показывает, как:

1. Загрузите существующий diagram.
1. Повторите выборочные формы страниц.
1. Примените фильтр, чтобы получить формы изображения.
1. Сохраните результат Visio diagram в локальном пространстве.
#### **Замена примера программирования формы изображения**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");
// Convert image into bytes array
byte[] imageBytes = File.ReadAllBytes(dataDir + "Picture.png");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Replace picture shape
            shape.ForeignData.Value = imageBytes;
        }
    }
}

// Save diagram
diagram.Save(dataDir + "ReplaceShapePicture_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Импортировать растровое изображение как форму Visio**
Aspose.Diagram for .NET API теперь позволяет разработчикам импортировать растровое изображение в виде формы.
### **Вставьте изображение BMP в Visio**
Код в приведенных ниже примерах показывает, как:

1. Создайте номер diagram.
1. Получить страницу Visio
1. Импорт растрового изображения в виде фигуры Visio
1. Сохраните номер diagram.
#### **Вставьте образец программирования изображения BMP**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Create a new diagram
Diagram diagram = new Diagram();

// Get page object by index
Page page0 = diagram.Pages[0];
// Set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import Bitmap image as Visio shape
page0.AddShape(pinX, pinY, width, hieght, new FileStream(dataDir + "image.bmp", FileMode.OpenOrCreate));

// Save Visio diagram
diagram.Save(dataDir + "InsertImageInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

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
