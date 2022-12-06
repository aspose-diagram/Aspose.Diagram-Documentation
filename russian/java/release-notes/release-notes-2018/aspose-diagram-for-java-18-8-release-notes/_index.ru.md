---
title: Aspose.Diagram for Java 18.8 Примечания к выпуску
type: docs
weight: 50
url: /ru/java/aspose-diagram-for-java-18-8-release-notes/
---
{{% alert color="primary" %}} 

 Эта страница содержит примечания к выпуску для[Aspose.Diagram for Java 18.8](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-8-release-notes/).

{{% /alert %}} 
## **Улучшения и изменения**

|**Ключ**|**Резюме**|**Категория**|
|:- |:- |:- |
|DIAGRAMJAVA-50611|Поддержка настройки локали с помощью API|Улучшение|
|DIAGRAMJAVA-50606|с VSDX по SVG - неправильная отрисовка стрелок|Ошибка|
|DIAGRAMJAVA-50610|Неправильное расположение текста на соединителях в выходном файле VSDX|Ошибка|
|DIAGRAMJAVA-50612|Невозможно открыть выходной файл VDX с помощью Visio Viewer 2010 Professional|Ошибка|
## **Public API и обратно несовместимые изменения**
Ниже приведен список любых изменений, внесенных в общедоступный номер API, таких как добавленные, переименованные, удаленные или устаревшие члены, а также любые несовместимые с предыдущими изменениями, внесенные в номер Aspose.Diagram for Java. Если у вас есть сомнения по поводу каких-либо перечисленных изменений, сообщите о них в в[Aspose.Diagram форум поддержки](https://forum.aspose.com/c/diagram/17).
#### **Добавлен setLocale в LoadOption.**
{{< highlight "java" >}}

         LoadOptions loadOptions = new LoadOptions( LoadFileFormat.VDX ); 

        loadOptions.setLocale(Locale.US);

        Diagram diagram = new Diagram("test.vdx", loadOptions); 

{{< /highlight >}}

устанавливает Локаль, используемую для diagram во время загрузки файла.
