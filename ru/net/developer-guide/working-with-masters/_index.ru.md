---
title: Работа с мастерами
type: docs
weight: 70
url: /ru/net/working-with-masters/
description: В этом разделе объясняется, как добавить мастер или получить информацию о мастере с помощью Aspose.Diagram.
---
## **Получение основной информации**
Мастер формы — это другое название трафарета Visio. С помощью Aspose.Diagram можно получить информацию о страницах, соединителях и мастерах. В этой статье объясняется, как получить идентификатор и имя по номеру diagram.

[Мастер](http://www.aspose.com/api/net/diagram/aspose.diagram/master) объект представляет собой[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) мастер объекта в diagram. Свойство Masters, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Master. Это свойство можно использовать для получения информации о мастере, т. е. идентификатора и имени мастера. Используйте свойство Page.Shapes, чтобы определить, какая фигура была унаследована эталонной фигурой.
### **Пример программирования получения основной информации**
Следующий фрагмент кода извлекает информацию об основных устройствах из файла diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-RetrieveMasterInfo-RetrieveMasterInfo.cs" >}}
## **Добавить мастер из трафарета фигур**
Трафарет — это набор фигур, связанных с определенным шаблоном Microsoft Office Visio. С помощью Aspose.Diagram можно добавить любой образец формы к рисунку из трафарета.
### **Добавить мастера**
[Мастер](http://www.aspose.com/api/net/diagram/aspose.diagram/master) объект представляет собой[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) мастер объекта в diagram. Метод AddMaster, предоставляемый классом Diagram, позволяет добавлять мастер из трафарета. Он предлагает следующие четыре способа:

- Путь к файлу трафарета и мастер-идентификатор.
- Путь к файлу трафарета и имя мастера.
- Поток файла трафарета и мастер-идентификатор.
- Поток файла трафарета и мастер-имя.
- Добавить мастер в diagram из источника diagram
#### **Добавить образец основного программирования**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-AddMasterFromStencil-AddMasterFromStencil.cs" >}}
## **Создать мастер с нуля**
 Aspose.Diagram API позволяет создать[Мастер](http://www.aspose.com/api/net/diagram/aspose.diagram/master) с нуля без всяких трафаретов, рисунков и шаблонов. Разработчики могут настроить создание Мастера. Метод AddMaster, предоставляемый классом Diagram, позволяет добавить мастер.
### **Создать основной образец программирования**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-CreateMasterFromScratch-CreateMasterFromScratch.cs" >}}
## **Получить мастер из файла Visio**
Иногда разработчикам необходимо получить подробную информацию о мастере чертежа Visio. Aspose.Diagram API поддерживает эту функцию.

 Aspose.Diagram for .NET предлагает[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)класс, представляющий чертеж Visio. Свойство Masters, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Master. Это свойство можно использовать для получения сведений об определенном мастере. Класс MasterCollection предоставляет методы GetMasterByName и GetMaster, которые можно вызывать для получения объекта Master.
### **Получение Мастер-объекта по ID**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetMaster класса Diagram.Masters.
#### **Образец программирования главного объекта по идентификатору**
В следующем примере показано, как получить мастер по идентификатору из чертежа Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyID-GetMasterbyID.cs" >}}
### **Получение главного объекта по имени**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetMasterByName класса Diagram.Masters.
#### **Образец программирования основного объекта по имени**
В следующем примере показано, как получить мастер-объект по имени из чертежа Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyName-GetMasterbyName.cs" >}}
## **Проверить наличие мастера в чертеже Visio**
Aspose.Diagram API поддерживает проверку наличия мастера в чертеже Visio. С помощью свойства MasterCollection разработчики могут проверить наличие мастера по его имени или идентификатору.

 Aspose.Diagram for .NET предлагает[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) класс, представляющий чертеж Visio. Свойство Masters, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Master. Это свойство можно использовать для проверки наличия определенного мастера. Класс MasterCollection предоставляет метод IsExist, который можно вызывать с помощью имени мастера или параметра ID.
### **Проверка присутствия Мастера по ID**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод IsExist класса Diagram.Masters.
#### **Образец программирования Master Presence by ID**
В следующем примере показано, как проверить наличие мастера по идентификатору в чертеже Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyID-CheckMasterPresencebyID.cs" >}}
### **Проверка присутствия мастера по имени**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод IsExist класса Diagram.Masters.
#### **Образец программирования Master Presence by Name**
В следующем примере показано, как проверить наличие мастера по имени из чертежа Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyName-CheckMasterPresencebyName.cs" >}}
