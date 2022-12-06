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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-ConfigureShapeLayers-ConfigureShapeLayers.cs" >}}
## **Добавьте новый слой в Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) позволяет разработчикам добавлять новые слои для организации пользовательских категорий фигур, а затем программно назначать фигуры этим слоям.[СлойКоллекция](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) класс предлагает метод Add, который позволяет добавить новый[Слой](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) на чертеже Visio. Разработчики могут устанавливать свойства слоя, инициализируя его объект класса.
### **Добавить пример программирования уровня**
Следующий фрагмент кода помогает добавить объекты слоя.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-AddLayer-AddLayer.cs" >}}
## **Получить все слои из Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) предоставляет разработчикам доступ к существующим слоям Visio diagram.[СтраницаЛист](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) собственность[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class позволяет получить список доступных слоев из Visio diagram, используя[СлойКоллекция](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) учебный класс.
### **Пример программирования извлечения слоев**
Следующий фрагмент кода помогает получить список слоев.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-RetrieveAllLayers-RetrieveAllLayers.cs" >}}
