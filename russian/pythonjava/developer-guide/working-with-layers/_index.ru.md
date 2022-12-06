---
title: Работа со слоями
type: docs
weight: 160
url: /ru/python-java/working-with-layers/
---
### **Настройка объектов Shape со слоями**
Aspose.Diagram для Python через Java позволяет настраивать объекты формы со слоями в Microsoft Office Visio diagram. Каждая фигура может принадлежать нескольким слоям, поэтому разработчики могут управлять формами в соответствии с потребностями конечного пользователя.

[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) Объект класса предлагает свойство LayerMember, которое позволяет добавлять/удалять объекты формы в/из слоев в чертеже Visio. Пользователи могут программно управлять этими свойствами с помощью Aspose.Diagram API следующим образом:

**Добавляйте, удаляйте и перемещайте объекты формы в/из слоев diagram.** 

Следующий фрагмент кода помогает добавлять, удалять и перемещать свойства объектов формы.
#### **Примеры программирования**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-ConfigureShapeLayers.py" >}}
### **Добавьте слой на странице Visio.**
Aspose.Diagram для Python через Java позволяет разработчикам добавлять новые слои для организации пользовательских категорий фигур, а затем программно назначать фигуры этим слоям.

[СлойКоллекция](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) класс предлагает метод add, который позволяет добавить новый[Слой](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) объект класса в[чертеж Visio](DrawingFlowChart.vsdx). Разработчики могут устанавливать свойства слоя, инициализируя его объект класса.

Следующий фрагмент кода помогает добавить объекты слоя.
#### **Примеры программирования**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-AddLayer.py" >}}

{{% alert color="primary" %}} 

Aspose.Diagram для Python через Java дает разработчикам доступ к существующим уровням Visio diagram.

{{% /alert %}} 
### **Получить все доступные слои**
[СтраницаЛист](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) собственность[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) класс позволяет получить список доступных слоев из[чертеж Visio](DrawingFlowChart.vsdx) с использованием[СлойКоллекция](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) учебный класс.

Следующий фрагмент кода помогает получить список слоев.
#### **Примеры программирования**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-RetrieveAllLayers.py" >}}
