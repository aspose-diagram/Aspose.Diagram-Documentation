---
title: Работа с пользовательскими ячейками
type: docs
weight: 100
url: /ru/java/working-with-user-defined-cells/
---
## **Чтение определяемых пользователем ячеек фигур Visio**
 Пользователи вставляют текстовые поля в фигуры для отображения дополнительной информации.**Пользовательские ячейки** является одной ветвью этих полей, и эта ветвь использует информацию, введенную в ячейку «Значение» раздела «Определяемые пользователем ячейки» в таблице свойств формы. Разработчики могут вставлять и читать все пользовательские ячейки, используя[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 Коллекция Users, предоставляемая[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) class поддерживает объект com.aspose.diagram.User.[Пользователь](https://reference.aspose.com/diagram/java/com.aspose.diagram/User) class можно использовать для чтения свойств. Есть несколько определяемых пользователем ячеек, как вы можете видеть на следующем изображении:

**Таблица с информацией об определяемых пользователем ячейках** 

![дело:изображение_альтернативный_текст](working-with-user-defined-cells_1.png)

Следующий код используется для чтения пользовательских ячеек.

На следующем изображении показан вывод после выполнения кода:

![дело:изображение_альтернативный_текст](working-with-user-defined-cells_2.png)
#### **Примеры программирования**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadUserdefinedCellsOfShape.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(1);
// extract user defined cells of the shape
for (User user :(Iterable<User>) shape.getUsers())
{
    System.out.println(user.getName() + ": " + user.getValue().getVal());
}

{{< /highlight >}}

### **Создать определяемую пользователем ячейку**
Aspose.Diagram for Java API позволяет разработчикам создавать определяемые пользователем ячейки в форме. В этом примере раздела описывается, как добавить необходимое количество строк с именами пользователей, присвоить строкам осмысленные имена и задать значения ячеек.

Метод add, предоставляемый коллекцией Users, можно использовать для создания определяемой пользователем ячейки в таблице форм. Он принимает один параметр.

Используйте следующий код в своем приложении Java, чтобы создать определяемую пользователем ячейку в таблице формы, используя Aspose.Diagram for Java.
#### **Примеры программирования**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateUserDefinedCellInShapeSheet.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(2);
        
// initialize user object
User user = new User();
user.setName("UserDefineCell");
user.getValue().setVal("800");
// add user-defined cell
shape.getUsers().add(user);

// save diagram
diagram.save(dataDir + "CreateUserDefinedCellInShapeSheet_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Получить пользовательские ячейки из таблицы форм**
Aspose.Diagram for Java API позволяет разработчикам извлекать пользовательские ячейки из таблицы форм. В этом примере раздела описывается, как получить все имена пользователей для всех фигур на чертеже.
### **Получить пользовательские ячейки**
 Методы getNameU(), getValue().getVal() и getPrompt().getValue(), предоставляемые[Пользователь](https://reference.aspose.com/diagram/java/com.aspose.diagram/User)class можно использовать для извлечения пользовательских ячеек из shapesheet.
#### **Извлечение ячеек из образцов программирования Shapesheet**
Используйте следующий код в своем приложении Java, чтобы получить все пользовательские ячейки из таблицы формы, используя Aspose.Diagram for Java.
#### **Примеры программирования**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateUserDefinedCellInShapeSheet.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(2);
        
// initialize user object
User user = new User();
user.setName("UserDefineCell");
user.getValue().setVal("800");
// add user-defined cell
shape.getUsers().add(user);

// save diagram
diagram.save(dataDir + "CreateUserDefinedCellInShapeSheet_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

