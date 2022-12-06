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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-UserDefinedCells-ReadUserdefinedCellsOfShape-ReadUserdefinedCellsOfShape.java" >}}
### **Создать определяемую пользователем ячейку**
Aspose.Diagram for Java API позволяет разработчикам создавать определяемые пользователем ячейки в форме. В этом примере раздела описывается, как добавить необходимое количество строк с именами пользователей, присвоить строкам осмысленные имена и задать значения ячеек.

Метод add, предоставляемый коллекцией Users, можно использовать для создания определяемой пользователем ячейки в таблице форм. Он принимает один параметр.

Используйте следующий код в своем приложении Java, чтобы создать определяемую пользователем ячейку в таблице формы, используя Aspose.Diagram for Java.
#### **Примеры программирования**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-UserDefinedCells-CreateUserDefinedCellInShapeSheet-CreateUserDefinedCellInShapeSheet.java" >}}
## **Получить пользовательские ячейки из таблицы форм**
Aspose.Diagram for Java API позволяет разработчикам извлекать пользовательские ячейки из таблицы форм. В этом примере раздела описывается, как получить все имена пользователей для всех фигур на чертеже.
### **Получить пользовательские ячейки**
 Методы getNameU(), getValue().getVal() и getPrompt().getValue(), предоставляемые[Пользователь](https://reference.aspose.com/diagram/java/com.aspose.diagram/User)class можно использовать для извлечения пользовательских ячеек из shapesheet.
#### **Извлечение ячеек из образцов программирования Shapesheet**
Используйте следующий код в своем приложении Java, чтобы получить все пользовательские ячейки из таблицы формы, используя Aspose.Diagram for Java.
#### **Примеры программирования**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-UserDefinedCells-CreateUserDefinedCellInShapeSheet-CreateUserDefinedCellInShapeSheet.java" >}}
