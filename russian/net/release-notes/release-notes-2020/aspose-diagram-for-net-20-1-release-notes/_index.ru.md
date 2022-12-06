---
title: Aspose.Diagram for .NET 20.1 Примечания к выпуску
type: docs
weight: 70
url: /ru/net/aspose-diagram-for-net-20-1-release-notes/
---
{{% alert color="primary" %}} 

Эта страница содержит примечания к выпуску для Aspose.Diagram for .NET 20.1.

{{% /alert %}} 
## **Улучшения и изменения**

|**Ключ**|**Резюме**|**Категория**|
|:- |:- |:- |
|DIAGRAMNET-51198|Тень на кнопке гиперссылки отображается неправильно при сохранении VSDM в SVG|Улучшение|
|DIAGRAMNET-51526|VSDX в PDF — градиентная заливка стрелок, потерянных в результирующем PDF|Улучшение|
|DIAGRAMNET-51539|Градиент в формах потерялся в выходном SVG|Улучшение|
|DIAGRAMNET-50705|VSD экспорт в SVG — фигуры метатипа превращаются в беспорядочные символы|Ошибка|
|DIAGRAMNET-51664|Файл повреждается после удаления неиспользуемой темы|Ошибка|
|DIAGRAMNET-51665|Изображения отображаются как X после удаления неиспользуемых тем|Ошибка|
|DIAGRAMNET-51684|При удалении неиспользуемых основных форм и стилей проблема возникает только с изображением.|Ошибка|
|DIAGRAMNET-51726|Отсутствует фоновое изображение (PowerPoint добавлено в VISIO) при удалении неиспользуемых эталонных фигур и стилей.|Ошибка|
|DIAGRAMNET-51737|Visio в Html - проблема с размером изображения|Ошибка|
|DIAGRAMNET-51743|Удаление личной информации из Visio - проблема с размером документа Visio|Ошибка|
|DIAGRAMNET-51745|Странная ошибка возникает в приложении WPF при преобразовании VSD в VSDX|Ошибка|

## **Public API и обратно несовместимые изменения**
- Добавленные страницы в LoadOptions — указывает индекс загружаемых страниц.



{{< highlight "java" >}}

Aspose.Diagram.LoadOptions options = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);

options.Pages = new ArrayList();

options.Pages.Add(0);

{{< /highlight >}}

- Добавлен SetFontSources в FontConfigs — устанавливает источники шрифтов.

{{< highlight "java" >}}

Aspose.Diagram.MemoryFontSource sc1 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource sc2 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource[]sc = new Aspose.Diagram.MemoryFontSource[]{ sc1, sc2 };

Aspose.Diagram.FontConfigs.SetFontSources(sc); 

{{< /highlight >}}
