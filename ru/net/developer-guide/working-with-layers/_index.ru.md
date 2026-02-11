---
title: Работа со слоями
type: docs
weight: 130
url: /ru/net/working-with-layers/
description: В этом разделе объясняется, как добавить или получить информацию о слое в форме visio с помощью Aspose.Diagram.
---
## **Настройте объекты формы со слоями в Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) позволяет настраивать объекты формы со слоями в Microsoft Office Visio diagram. Каждая фигура может принадлежать нескольким слоям, поэтому разработчики могут управлять формами в соответствии с потребностями конечного пользователя.[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) объект класса предлагает свойство LayerMember, которое позволяет добавлять и удалять объекты формы в слои и из слоев в чертеже Visio. Пользователи могут программно управлять этими свойствами с помощью Aspose.Diagram API следующим образом:
### **Пример программирования конфигурации объектов формы**
Следующий фрагмент кода помогает добавлять, удалять и перемещать свойства объекта формы.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the shapes
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name.ToLower() == "shape1")
    {
        // Add shape1 in first two layers. Here "0;1" are indexes of the layers
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "0;1";
    }
    else if (shape.Name.ToLower() == "shape2")
    {
        // Remove shape2 from all the layers
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "";
    }
    else if (shape.Name.ToLower() == "shape3")
    {
        // Add shape3 in first layer. Here "0" is index of the first layer
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "0";
    }
}
// Save diagram
diagram.Save(dataDir + "ConfigureShapeLayers_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Добавьте новый слой в Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) позволяет разработчикам добавлять новые слои для организации пользовательских категорий фигур, а затем программно назначать фигуры этим слоям.[СлойКоллекция](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) класс предлагает метод Add, который позволяет добавить новый[Слой](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) на чертеже Visio. Разработчики могут устанавливать свойства слоя, инициализируя его объект класса.
### **Добавить пример программирования уровня**
Следующий фрагмент кода помогает добавить объекты слоя.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object
Layer layer = new Layer();
// Set Layer name
layer.Name.Value = "Layer1";
// Set Layer Visibility
layer.Visible.Value = BOOL.True;
// Set the color checkbox of Layer
layer.IsColorChecked = BOOL.True;
// Add Layer to the particular page sheet
page.PageSheet.Layers.Add(layer);

// Get shape by ID
Shape shape = page.Shapes.GetShape(3);
// Assign shape to this new Layer
shape.LayerMem.LayerMember.Value = layer.IX.ToString();
// Save diagram
diagram.Save(dataDir + "AddLayer_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Получить все слои из Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) предоставляет разработчикам доступ к существующим слоям Visio diagram.[СтраницаЛист](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) собственность[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class позволяет получить список доступных слоев из Visio diagram, используя[СлойКоллекция](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) учебный класс.
### **Пример программирования извлечения слоев**
Следующий фрагмент кода помогает получить список слоев.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Layer layer in page.PageSheet.Layers)
{
    Console.WriteLine("Name: " + layer.Name.Value);
    Console.WriteLine("Visibility: " + layer.Visible.Value);
    Console.WriteLine("Status: " + layer.Status.Value);
}

{{< /highlight >}}
```
