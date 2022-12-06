---
title: Aspose.Diagram for .NET 20.2 Примечания к выпуску
type: docs
weight: 60
url: /ru/net/aspose-diagram-for-net-20-2-release-notes/
---
{{% alert color="primary" %}} 

Эта страница содержит примечания к выпуску для Aspose.Diagram for .NET 20.2.

{{% /alert %}} 
## **Улучшения и изменения**

|**Ключ**|**Резюме**|**Категория**|
|:- |:- |:- |
|DIAGRAMNET-51747|Изменения файлов после преобразования Visio vsd->vsdx|Улучшение|
|DIAGRAMNET-51750|Добавление флага «HasHiddenInfo»|Улучшение|
|DIAGRAMNET-51748|Добавить PNG в Diagram - потеря прозрачности|Ошибка|
|DIAGRAMNET-51749|Ошибка возникает при сохранении документа Visio|Ошибка|
|DIAGRAMNET-51751|VSDX в PNG - показано дополнительное изображение|Ошибка|
|DIAGRAMNET-51752|VSDX в PNG — показано дополнительное пространство|Ошибка|
|DIAGRAMNET-51753|VSDX в PNG - меняется положение значков|Ошибка|
|DIAGRAMNET-51754|VSDX в PNG — положение значка вопросительного знака изменено|Ошибка|
|DIAGRAMNET-51762|Сгенерированный PDF-файл отличается от введенного Visio diagram|Ошибка|
|DIAGRAMNET-51763|VSDX в PNG — в выводе отсутствует информация|Ошибка|
## ` `**Public API и обратно несовместимые изменения**
` `Ниже приведен список любых изменений, внесенных в общедоступный API, таких как добавленные, переименованные, удаленные или устаревшие члены, а также любые несовместимые с предыдущими изменениями, внесенные в Aspose.Diagram for .NET. Если у вас есть сомнения по поводу каких-либо перечисленных изменений, сообщите об этом на форум поддержки Aspose.Diagram.
### **Добавлен EnlargePage в ImageSaveOptions**
- Указывает, следует ли увеличивать страницу

{{< highlight "java" >}}

 Aspose.Diagram.Saving.ImageSaveOptions opt = new Aspose.Diagram.Saving.ImageSaveOptions(Aspose.Diagram.SaveFileFormat.PNG);

opt.EnlargePage = false;

{{< /highlight >}}
### **Добавлен HasHiddenInfo в Diagram**
- Указывает, содержит ли этот номер diagram скрытую информацию.



{{< highlight "java" >}}

 diagram.HasHiddenInfo();

{{< /highlight >}}




