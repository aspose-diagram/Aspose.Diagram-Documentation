---
title: Работа с пользовательскими ячейками
type: docs
weight: 150
url: /ru/net/working-with-user-defined-cells/
description: В этом разделе объясняется, как читать определяемые пользователем ячейки фигур visio с помощью Aspose.Diagram.
---
## **Чтение определяемых пользователем ячеек фигур Visio**
 Пользователи вставляют текстовые поля в фигуры для отображения дополнительной информации.**Пользовательские ячейки** является одной ветвью этих полей, и эта ветвь использует информацию, введенную в ячейку «Значение» раздела «Определяемые пользователем ячейки» в таблице свойств формы. Разработчики могут вставлять и читать все пользовательские ячейки, используя[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Получить пользовательские поля ячеек**
 Коллекция пользователей, представленная[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) класс поддерживает объект Aspose.Diagram.User. Это свойство можно использовать для чтения определяемых пользователем ячеек фигуры Visio, доступных в разделе «Определяемые пользователем ячейки» таблицы свойств фигуры.

![дело:изображение_альтернативный_текст](working-with-user-defined-cells_1.png)
#### **Получить образец программирования ячеек**
Следующий фрагмент кода позволяет разработчикам читать пользовательские поля ячеек.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UserDefinedCells();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(1);
// Extract user defined cells of the shape
foreach (User user in shape.Users)
{
    Console.WriteLine(user.Name + ": " + user.Value.Val);
}

{{< /highlight >}}



На этом изображении показан вывод после запуска приведенного выше кода:

![дело:изображение_альтернативный_текст](working-with-user-defined-cells_2.png)
## **Создать определяемую пользователем ячейку в ShapeSheet**
[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/) позволяет создать определяемую пользователем ячейку в форме. В этом примере раздела описывается, как разработчики могут добавлять столько строк User.name, сколько им нужно, назначать значимые имена строкам и задавать значения ячеек.
### **Создать определяемую пользователем ячейку**
Метод Add, предоставляемый коллекцией пользователей, можно использовать для создания определяемой пользователем ячейки в таблице форм. Он принимает один параметр.
#### **Создайте пример программирования ячейки**
Используйте следующий пример кода в своем приложении .NET, чтобы создать пользовательскую ячейку в таблице формы, используя Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UserDefinedCells();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(2);
            
// Initialize user object
User user = new User();
user.Name = "UserDefineCell";
user.Value.Val = "800";
// Add user-defined cell
shape.Users.Add(user);

// Save diagram
diagram.Save(dataDir + "CreateUserDefinedCellInShapeSheet_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Получить пользовательские ячейки из таблицы форм**
Aspose.Diagram for .NET API позволяет извлекать пользовательские ячейки из таблицы форм. В этом примере раздела описывается, как разработчики могут получить все User.name для всех фигур на чертеже.
### **Получить пользовательские ячейки**
Свойства NameU, Value.Val и Prompt.Value, предоставляемые классом User, можно использовать для извлечения пользовательских ячеек из таблицы формы.
#### **Извлечение ячеек из образцов программирования Shapesheet**
Используйте следующий код в своем приложении .NET, чтобы получить все пользовательские ячейки из таблицы формы, используя Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UserDefinedCells();
int count = 0;
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Iterate through pages
foreach (Aspose.Diagram.Page objPage in diagram.Pages)
{
    // Iterate through shapes
    foreach (Aspose.Diagram.Shape objShape in objPage.Shapes)
    {
        Console.WriteLine(objShape.NameU);
        // Iterate through user-defined cells
        foreach (Aspose.Diagram.User objUserField in objShape.Users)
        {
            count++;
            Console.WriteLine(count + " - Name: " + objUserField.NameU + " Value: " + objUserField.Value.Val + " Prompt: " + objUserField.Prompt.Value);
        }
    }
}  

{{< /highlight >}}

