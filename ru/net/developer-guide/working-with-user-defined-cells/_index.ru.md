﻿---
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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-User-defined-Cells-ReadUserdefinedCellsOfShape-ReadUserdefinedCellsOfShape.cs" >}}


На этом изображении показан вывод после запуска приведенного выше кода:

![дело:изображение_альтернативный_текст](working-with-user-defined-cells_2.png)
## **Создать определяемую пользователем ячейку в ShapeSheet**
[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/) позволяет создать определяемую пользователем ячейку в форме. В этом примере раздела описывается, как разработчики могут добавлять столько строк User.name, сколько им нужно, назначать значимые имена строкам и задавать значения ячеек.
### **Создать определяемую пользователем ячейку**
Метод Add, предоставляемый коллекцией пользователей, можно использовать для создания определяемой пользователем ячейки в таблице форм. Он принимает один параметр.
#### **Создайте пример программирования ячейки**
Используйте следующий пример кода в своем приложении .NET, чтобы создать пользовательскую ячейку в таблице формы, используя Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-User-defined-Cells-CreateUserDefinedCellInShapeSheet-CreateUserDefinedCellInShapeSheet.cs" >}}
## **Получить пользовательские ячейки из таблицы форм**
Aspose.Diagram for .NET API позволяет извлекать пользовательские ячейки из таблицы форм. В этом примере раздела описывается, как разработчики могут получить все User.name для всех фигур на чертеже.
### **Получить пользовательские ячейки**
Свойства NameU, Value.Val и Prompt.Value, предоставляемые классом User, можно использовать для извлечения пользовательских ячеек из таблицы формы.
#### **Извлечение ячеек из образцов программирования Shapesheet**
Используйте следующий код в своем приложении .NET, чтобы получить все пользовательские ячейки из таблицы формы, используя Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-User-defined-Cells-RetrieveUserDefinedCells-RetrieveUserDefinedCells.cs" >}}
