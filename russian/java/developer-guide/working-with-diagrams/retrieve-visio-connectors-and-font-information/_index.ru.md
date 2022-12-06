﻿---
title: Получить Visio соединители и информацию о шрифтах
type: docs
weight: 20
url: /ru/java/retrieve-visio-connectors-and-font-information/
---
## **Получение информации о соединителе**
 Aspose.Diagram for Java предоставляет механизмы для получения информации - ID и имя - о[страницы](/diagram/ru/java/retrieve-get-copy-and-insert-a-page/) а также[мастер](). Он также позволяет получить информацию о соединителях, элементах, которые связывают фигуры.

[Соединять](https://reference.aspose.com/diagram/java/com.aspose.diagram/connect) Объект представляет соединитель, который соединяет две фигуры на странице рисования Visio. Свойство Connects, предоставляемое[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class поддерживает набор объектов Aspose.Diagram.Connect. Это свойство можно использовать для получения сведений об идентификаторе и имени соединителя.

**Окно консоли, показывающее вывод кода ниже.** 

![дело:изображение_альтернативный_текст](retrieve-visio-connectors-and-font-information_1.png)
### **Образец программирования**
Следующий фрагмент кода извлекает информацию о соединителях в файле diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RetrieveConnectorInfo-RetrieveConnectorInfo.java" >}}
## **Получение информации о шрифте**
 Aspose.Diagram имеет механизмы для получения информации об элементах, составляющих diagram, из[страницы](/diagram/ru/java/retrieve-get-copy-and-insert-a-page/), [трафареты](), [соединители](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection)а также шрифты. В этой статье показано, как узнать, какие шрифты используются в файле diagram.

[Шрифт](https://reference.aspose.com/diagram/java/com.aspose.diagram/font) объект представляет собой шрифт, который либо применяется к тексту в документе, либо доступен для использования в системе.

Объект Font сопоставляет имя (например, «Arial») с идентификатором шрифта (например, 3), который Microsoft Visio хранится в ячейке «Шрифт» в разделе «Символ» фигуры, содержащей текст, отформатированный с помощью этого шрифта. Идентификаторы шрифтов могут меняться при открытии документа в разных системах или при установке или удалении шрифтов.
### **Получение примера программирования шрифтов**
Следующий фрагмент кода извлекает информацию о шрифте из файла Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RetrieveFontInfo-RetrieveFontInfo.java" >}}

![дело:изображение_альтернативный_текст](retrieve-visio-connectors-and-font-information_2.png)
### **Получение каталога шрифтов по умолчанию**
Aspose.Diagram for Java API также позволяет получить путь к каталогу шрифтов по умолчанию, используя метод getDefaultFontDir() класса Diagram. Следующий фрагмент кода извлекает каталог шрифтов по умолчанию из файла Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-GetDefaultFontDirectory-GetDefaultFontDirectory.java" >}}
