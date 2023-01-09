---
title: Aspose.Diagram for Java 20.10 Примечания к выпуску
type: docs
weight: 10
url: /ru/java/aspose-diagram-for-java-20-10-release-notes/
---
{{% alert color="primary" %}}

Эта страница содержит информацию о выпуске для Aspose.Diagram for Java 20.10.

{{% /alert %}}
## **Улучшения и изменения**  ##

|**Ключ**|**Резюме**|**Категория**|
|:- |:- |:- |
|DIAGRAMJAVA-50457|Текстовые элементы смещаются при преобразовании страниц VSD в SVG.|Улучшение|

## Публичный API Изменения
* Добавлен IsExportScaleInMatrix в SVGSaveOptions - определяет, нужно ли экспортировать масштаб в матрицу или нет.
```
SVGSaveOptions o = new SVGSaveOptions();
o.setExportScaleInMatrix(false);
```
