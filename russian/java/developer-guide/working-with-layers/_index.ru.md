---
title: Работа со слоями
type: docs
weight: 160
url: /ru/java/working-with-layers/
---
### **Настройка объектов Shape со слоями**
Aspose.Diagram for Java позволяет настраивать объекты формы со слоями в Microsoft Office Visio diagram. Каждая фигура может принадлежать нескольким слоям, поэтому разработчики могут управлять формами в соответствии с потребностями конечных пользователей.

[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) Объект класса предлагает свойство LayerMember, которое позволяет добавлять/удалять объекты формы в/из слоев в чертеже Visio. Пользователи могут программно управлять этими свойствами с помощью Aspose.Diagram API следующим образом:

**Добавляйте, удаляйте и перемещайте объекты формы в/из слоев diagram.** 

![дело:изображение_альтернативный_текст](working-with-layers_1.png)

Следующий фрагмент кода помогает добавлять, удалять и перемещать свойства объектов формы.
#### **Примеры программирования**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Layers-ConfigureShapeLayers-ConfigureShapeLayers.java" >}}
### **Добавьте слой на странице Visio.**
Aspose.Diagram for Java позволяет разработчикам добавлять новые слои для организации пользовательских категорий фигур, а затем программно назначать фигуры этим слоям.

[СлойКоллекция](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) класс предлагает метод add, который позволяет добавить новый[Слой](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)объект класса на чертеже Visio. Разработчики могут устанавливать свойства слоя, инициализируя его объект класса.

Следующий фрагмент кода помогает добавить объекты слоя.
#### **Примеры программирования**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Layers-AddLayer-AddLayer.java" >}}

{{% alert color="primary" %}} 

Aspose.Diagram for Java предоставляет разработчикам доступ к существующим уровням Visio diagram.

{{% /alert %}} 
### **Получить все доступные слои**
[СтраницаЛист](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) собственность[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) класс позволяет получить список доступных слоев из Visio diagram с помощью[СлойКоллекция](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) учебный класс.

Следующий фрагмент кода помогает получить список слоев.
#### **Примеры программирования**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Layers-RetrieveAllLayers-RetrieveAllLayers.java" >}}
