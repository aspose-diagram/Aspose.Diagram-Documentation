---
title: Aspose.Diagram for .NET 21.11 Примечания к выпуску
type: docs
weight: 2
url: /ru/net/aspose-diagram-for-net-21-11-release-notes/
---
{{% alert color="primary" %}} 

Эта страница содержит примечания к выпуску для Aspose.Diagram for .NET 21.11.

{{% /alert %}} 
## **Улучшения и изменения**

|**Ключ**|**Резюме**|**Категория**|
|:- |:- |:- |
|DIAGRAMNET-51111|Градиентная заливка кругов неверна при преобразовании VDX в EMF|Улучшение|
|DIAGRAMNET-52377|Добавлена поддержка загрузки vsd со старой версией 3.|Улучшение|
|DIAGRAMNET-51364|VSDX в PNG - отсутствует текст объекта OLE Embedded|Ошибка|
|DIAGRAMNET-52329|VSDX в HTML — эмодзи отсутствуют в выводе|Ошибка|
|DIAGRAMNET-52345|Нижний колонтитул верхнего колонтитула теряется после сохранения файла Diagram|Ошибка|
|DIAGRAMNET-52349|Visio в HTML — левый и правый края обрезаны|Ошибка|
|DIAGRAMNET-52374|ArgumentOutOfRangeException при сохранении в PDF|Ошибка|
|DIAGRAMNET-52386|Почему некоторые страницы diagram могут быть продублированы, а некоторые не могут использовать Page.Copy()?|Ошибка|

## **Public API и обратно несовместимые изменения**
Ниже приведен список любых изменений, внесенных в общедоступный номер API, таких как добавленные, переименованные, удаленные или устаревшие члены, а также любые несовместимые с предыдущими изменениями, внесенные в номер Aspose.Diagram for .NET. Если у вас есть сомнения по поводу каких-либо перечисленных изменений, сообщите об этом на форум поддержки Aspose.Diagram.


### **Добавляет PresetTheme в форму**
- Примените предустановленную тему к этой фигуре.

{{< highlight "java" >}}

shape.PresetTheme = PresetThemeValue.Bubble;

{{< /highlight >}}


### **Добавляет PresetThemeVariant в форму**
- Применить предустановленный вариант темы к этой фигуре

{{< highlight "java" >}}

shape.PresetThemeVariant = PresetThemeVariantValue.Variant1;

{{< /highlight >}}

### **Добавляет PresetThemeQuickStyle в форму**
- Применить готовый вариант быстрого стиля темы к этой фигуре

{{< highlight "java" >}}

 shape.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle1;

{{< /highlight >}}
