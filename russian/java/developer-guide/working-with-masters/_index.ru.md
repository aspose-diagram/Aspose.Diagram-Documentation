---
title: Работа с мастерами
type: docs
weight: 30
url: /ru/java/working-with-masters/
---
## **Получение основной информации**
Мастер формы — это другое название трафарета Visio. С помощью Aspose.Diagram можно получить информацию о страницах, соединителях, а также мастерах. В этой статье объясняется, как получить идентификатор и имя по номеру diagram.

[Мастер](https://reference.aspose.com/diagram/java/com.aspose.diagram/master) объект представляет собой[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)мастер объекта в diagram. Свойство Masters, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Master. Это свойство можно использовать для получения информации о мастере, т. е. идентификатора и имени мастера.

Используйте свойство Page.Shapes, чтобы определить, какая фигура была унаследована эталонной фигурой.

**Окно консоли, показывающее вывод кода.** 

![дело:изображение_альтернативный_текст](http://i.imgur.com/DPn5sP9.png)
### **Пример программирования получения основной информации**
Следующий фрагмент кода извлекает информацию об основных устройствах из файла diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-RetrieveMasterInfo-RetrieveMasterInfo.java" >}}
## **Добавить мастер из трафарета фигур**
Трафарет — это набор фигур, связанных с определенным шаблоном Microsoft Office Visio. С помощью Aspose.Diagram можно добавить любой образец формы к рисунку из трафарета.
### **Добавить мастера**
Объект Master представляет мастер объекта Shape в diagram. Метод AddMaster, предоставляемый классом Diagram, позволяет добавлять мастер из трафарета. Он предлагает следующие четыре способа:

- Путь к файлу трафарета и мастер-идентификатор.
- Путь к файлу трафарета и имя мастера.
- Поток файла трафарета и мастер-идентификатор.
- Поток файла трафарета и мастер-имя.
- Добавить мастер в diagram из источника diagram
#### **Добавить образец основного программирования**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-AddMasterFromStencil-AddMasterFromStencil.java" >}}
## **Создать мастер с нуля**
Aspose.Diagram API позволяет создать мастер с нуля без использования трафарета, рисунка или шаблона. Разработчики могут настроить создание Мастера. Метод addMaster, предоставляемый классом Diagram, позволяет добавить мастер.
#### **Создать основной образец программирования**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CreateMasterfromScratch-CreateMasterfromScratch.java" >}}

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-BASE64Encoder-BASE64Encoder.java" >}}
## **Получить мастер из файла Visio**
Иногда разработчикам необходимо получить подробную информацию о мастере чертежа Visio. Aspose.Diagram API поддерживает эту функцию.

 Aspose.Diagram for Java предлагает[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)класс, представляющий чертеж Visio. Свойство Masters, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Master. Это свойство можно использовать для получения сведений об определенном мастере. Класс MasterCollection предоставляет методы GetMasterByName и GetMaster, которые можно вызывать для получения объекта Master.
### **Получение Мастер-объекта по ID**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetMaster класса Diagram.Masters.
#### **Образец программирования главного объекта по идентификатору**
В следующем примере показано, как получить мастер по идентификатору из чертежа Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-GetMasterbyID-GetMasterbyID.java" >}}
### **Получение главного объекта по имени**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetMasterByName класса Diagram.Masters.
#### **Образец программирования основного объекта по имени**
В следующем примере показано, как получить мастер-объект по имени из чертежа Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-GetMasterbyName-GetMasterbyName.java" >}}
## **Проверить наличие мастера в чертеже Visio**
Aspose.Diagram API поддерживает проверку наличия мастера в чертеже Visio. С помощью свойства MasterCollection разработчики могут проверить наличие мастера по его имени или идентификатору.

 Aspose.Diagram for Java предлагает[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) класс, представляющий чертеж Visio. Свойство Masters, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Master. Это свойство можно использовать для проверки наличия определенного мастера. Класс MasterCollection предоставляет метод IsExist, который можно вызывать с помощью имени мастера или параметра ID.
### **Проверка присутствия Мастера по ID**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод IsExist класса Diagram.Masters.
#### **Образец программирования Master Presence by ID**
В следующем примере показано, как проверить наличие мастера по идентификатору в чертеже Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CheckMasterPresencebyID-CheckMasterPresencebyID.java" >}}
### **Проверка присутствия мастера по имени**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод IsExist класса Diagram.Masters.
#### **Образец программирования Master Presence by Name**
В следующем примере показано, как проверить наличие мастера по имени из чертежа Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Masters-CheckMasterPresencebyName-CheckMasterPresencebyName.java" >}}
