---
title: Aspose.Diagram for Java 18.2 Примечания к выпуску
type: docs
weight: 110
url: /ru/java/aspose-diagram-for-java-18-2-release-notes/
---
{{% alert color="primary" %}} 

 Эта страница содержит примечания к выпуску для[Aspose.Diagram for Java 18.2](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-2-release-notes/).

{{% /alert %}} 
## **Улучшения и изменения**

|**Ключ**|**Резюме**|**Категория**|
|:- |:- |:- |
|DIAGRAMJAVA-50587|Добавлена поддержка получения относительного элемента Char текстовой части.|Улучшение|
|DIAGRAMJAVA-50478|Соединительные линии проходят через другие формы при преобразовании VDX в VSDM.|Ошибка|
|DIAGRAMJAVA-50581|VSDX в PDF - неправильное отображение фигур|Ошибка|
|DIAGRAMJAVA-50582|Выход VSDX - соединительные линии не прямые|Ошибка|
|DIAGRAMJAVA-50583|VSD импорт — ошибка в элементе VisioDocument|Ошибка|
|DIAGRAMJAVA-50584|VDX импорт — ошибка в элементе VisioDocument|Ошибка|
|DIAGRAMJAVA-50585|VSD импорт — ошибка в элементе VisioDocument|Ошибка|
|DIAGRAMJAVA-50586|VSDX в SVG - неправильный цвет границы формы|Ошибка|
### **Добавляет метод getInheritChars в класс Shape.**
Он содержит значения char для формы, наследуемой основной формой.

{{< highlight "java" >}}

 CharCollection charCollection = shape.getInheritChars();

{{< /highlight >}}
