---
title: Aspose.Diagram for .NET 19.2 Примечания к выпуску
type: docs
weight: 110
url: /ru/net/aspose-diagram-for-net-19-2-release-notes/
---
{{% alert color="primary" %}} 

Эта страница содержит примечания к выпуску для[Aspose.Diagram for .NET 19.2](https://www.nuget.org/packages/Aspose.Diagram/19.2.0)

{{% /alert %}} 
## **Улучшения и изменения**

|**Ключ**|**Резюме**|**Категория**|
|:- |:- |:- |
|DIAGRAMNET-50009|Форма сердца перепутана при экспорте чертежа VSD в формате файла PDF.|Улучшение|
|DIAGRAMNET-50010|VSD в PDF экспортирует несколько зигзагообразных линий с совпадающими точками вместо одной кривой|Улучшение|
|DIAGRAMNET-51257|Добавлена поддержка линии NUBRS при экспорте чертежа.|Улучшение|
|DIAGRAMNET-51611|Не удалось правильно получить Prop.Prompt.Value|Улучшение|
|DIAGRAMNET-50355|Изогнутые линии экспортируются как прямые|Ошибка|
|DIAGRAMNET-50702|VSDX экспорт в PDF - изогнутые разъемы превращаются в прямые|Ошибка|
|DIAGRAMNET-51348|VSDX в PDF - Неверное отображение букв|Ошибка|
|DIAGRAMNET-51399|VSD в PNG - изогнутая линия преобразуется в прямую|Ошибка|
|DIAGRAMNET-51448|VSD в PNG - эллипс отсутствует вокруг слова network|Ошибка|
|DIAGRAMNET-51472|VSD в PDF - изогнутые линии экспортируются как прямые|Ошибка|
|DIAGRAMNET-51507|VSDX в PNG — в выходных данных отсутствуют закрашенные овалы|Ошибка|
|DIAGRAMNET-51508|VSDX в SVG — в выводе отсутствуют заполненные овалы|Ошибка|
|DIAGRAMNET-51537|VSDX в SVG — изогнутые соединители становятся прямыми соединителями, когда VSDX преобразуется в PDF|Ошибка|
|DIAGRAMNET-51540|Края формы были изменены на квадратные после преобразования|Ошибка|
|DIAGRAMNET-51577|VISIO в SVG — неправильный вывод|Ошибка|
|DIAGRAMNET-51592|Изогнутые линии превращаются в прямые при преобразовании|Ошибка|
|DIAGRAMNET-51600|Прямые линии становятся шипами при сохранении diagram в другом формате.|Ошибка|
|DIAGRAMNET-51604|Ошибка преобразования VSDX в PDF — черные многоточия|Ошибка|
|DIAGRAMNET-51605|Обновите ссылки API и добавьте сведения о методе Shape.SetAngle().|Ошибка|
|DIAGRAMNET-51610|VSDX в SVG - текст не отображается в правильном шрифте|Ошибка|
## **Public API и обратно несовместимые изменения**
Ниже приведен список любых изменений, внесенных в общедоступный номер API, таких как добавленные, переименованные, удаленные или устаревшие члены, а также любые несовместимые с предыдущими изменениями, внесенные в номер Aspose.Diagram for .NET. Если у вас есть сомнения по поводу каких-либо перечисленных изменений, сообщите о них в в[Aspose.Diagram форум поддержки](https://forum.aspose.com/c/diagram/17).
### **Добавить InheritProps в форму**
Содержит реквизиты для формы, наследуемой основной формой.

{{< highlight "java" >}}

  foreach (Aspose.Diagram.Prop prop in shape.InheritProps)

{

    Console.WriteLine(prop.Name);

    Console.WriteLine(prop.Label.Value);

    Console.WriteLine(prop.Prompt.Value);

    Console.WriteLine(prop.Type.Value.ToString());

    Console.WriteLine(prop.Value.Val);

    Console.WriteLine(prop.Format.Value);

}

{{< /highlight >}}
