---
title: Работа с формой типа соединителя
type: docs
weight: 80
url: /ru/java/working-with-connector-type-shape/
---
## **Установите внешний вид формы типа соединителя в Visio**
В этом разделе подробно описывается, как разработчики могут изменить внешний вид формы типа динамического соединителя, используя Aspose.Diagram for Java.
### **Установить внешний вид соединителя**
 Метод SetConnectorsType, предоставляемый[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class можно использовать для установки внешнего вида формы типа соединителя.

В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. получить конкретную страницу.
1. получить конкретную форму разъема.
1. задать внешний вид формы.
1. сохранить diagram
#### **Пример программирования внешнего вида коннектора**
Используйте следующий код в своем приложении Java, чтобы настроить внешний вид формы типа соединителя, используя Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetConnectorAppearance.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//get a particular page
Page page = diagram.getPages().getPage("Page-3");
//get a dynamic connector type shape by id
Shape shape = page.getShapes().getShape(18);
// set dynamic connector appearance
shape.setConnectorsType(ConnectorsTypeValue.STRAIGHT_LINES);

//saving Visio diagram
diagram.save(dataDir + "SetConnectorAppearance_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Выберите вариант перенаправления формы соединителя**
 Свойство ConFixedCode, предоставляемое[Макет](https://reference.aspose.com/diagram/java/com.aspose.diagram/layout) класс можно использовать для выбора варианта перенаправления. Свойство Layout, предоставляемое[Форма](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) класс, будет использоваться.

|<p>**Как выбрать параметры перенаправления** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/1O70sSA.png)</p>|
|:- |
В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. получить конкретную страницу.
1. получить конкретную форму разъема.
1. установить параметры перенаправления.
1. сохранить diagram.
### **Пример программирования выбора варианта перенаправления**
Используйте следующий код в своем приложении Java, чтобы выбрать параметр повторной маршрутизации формы соединителя, используя Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RerouteConnectors.class);   
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// get a particular connector shape
Shape shape = page.getShapes().getShape(18);
// set reroute option
shape.getLayout().getConFixedCode().setValue(ConFixedCodeValue.NEVER_REROUTE);

// save Visio diagram
diagram.save(dataDir + "RerouteConnectors_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
