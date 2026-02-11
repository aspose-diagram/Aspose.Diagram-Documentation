---
title: Изменить свойства слоя
type: docs
weight: 130
url: /ru/net/change-properties-layer/
description: В этом разделе объясняется, как изменить свойства слоя с помощью Aspose.Diagram.
---
## **Изменить свойства слоя в Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) позволяет изменять свойства слоя в Microsoft Office Visio diagram. Каждая фигура может принадлежать нескольким слоям, поэтому разработчики могут изменять свойства слоя в соответствии с потребностями конечного пользователя.[СтраницаЛист](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)объект класса предлагает слои, которые позволяют добавлять и удалять объекты слоев в чертеже Visio. Пользователи могут управлять[Слой](https://reference.aspose.com/diagram/net/aspose.diagram/layer) свойства программно с использованием Aspose.Diagram API следующим образом:
### **Пример программирования изменения свойств слоя**
Следующий фрагмент кода помогает изменить свойства слоя.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Aspose.Diagram.Layer layer in Page.PageSheet.Layers)
{
    layer.Visible.Value = Aspose.Diagram.BOOL.True;
    layer.Print.Value = Aspose.Diagram.BOOL.True;
}
// Save diagram
diagram.Save(dataDir + "ChangeLayerProperty_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
