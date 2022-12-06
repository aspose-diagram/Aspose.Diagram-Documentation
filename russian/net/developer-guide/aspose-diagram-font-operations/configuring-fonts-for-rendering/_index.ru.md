---
title: Настройка шрифтов для рендеринга
type: docs
weight: 10
url: /ru/net/configuring-fonts-for-rendering/
---
## **Возможные сценарии использования**

API-интерфейсы Aspose.Diagram позволяют отображать страницы в форматах изображений, а также преобразовывать их в форматы PDF и XPS. Чтобы максимизировать точность преобразования, необходимо, чтобы шрифты, используемые в электронной таблице, были доступны в каталоге шрифтов операционной системы по умолчанию. Если необходимые шрифты отсутствуют, API-интерфейсы Aspose.Diagram попытаются заменить требуемые шрифты доступными.

## **Выбор шрифтов**

Ниже показан процесс, которому Aspose.Diagram API следуют за сценой.

1. API пытается найти шрифты в файловой системе, соответствующие точному имени шрифта, используемому в электронной таблице.
1.  Если API не может найти шрифт, определенный в**[SaveOptions.DefaultFont] (https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/defaultfont/)** свойство, он пытается использовать шрифт, указанный в**[FontConfigs.DefaultFontName] (https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)**имущество.
1.  Если API не может найти шрифт, определенный в**[FontConfigs.DefaultFontName] (https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)** свойство, он пытается выбрать наиболее подходящие шрифты из всех доступных шрифтов.
1. Наконец, если API не может найти шрифты в файловой системе, страница отображается с использованием Times New Roman.

## **Установить папки пользовательских шрифтов**

 Aspose.Diagram API-интерфейсы выполняют поиск требуемых шрифтов в каталоге шрифтов операционной системы по умолчанию. Если требуемые шрифты недоступны в системном каталоге шрифтов, API-интерфейсы выполняют поиск в пользовательских (определяемых пользователем) каталогах.**[Конфигурации шрифтов] (https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/)** class предоставил несколько способов установки пользовательских каталогов шрифтов, как описано ниже.

1. **[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)**: этот метод удобен, если необходимо установить только одну папку.

1. **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)**этот метод удобен, когда шрифты находятся в нескольких папках, и пользователь хочет установить все папки по отдельности, а не объединять все шрифты в одной папке.
1. **[FontConfigs.SetFontSources] (https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontsources/)**: этот механизм полезен, когда пользователь хочет загрузить шрифты из нескольких папок или из одного файла шрифта или данных шрифта из массива байтов.

{{% alert color="primary" %}}

 Оба**[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)** & **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)** методы принимают второй параметр логического типа. Прохождение**истинный** поскольку второй параметр будет указывать API Aspose.Diagram для поиска файлов шрифтов во вложенных папках.

{{% /alert %}}

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-OS-Fonts-Location-SetCustomFontFolders-SetCustomFontFolders.cs" >}}

{{% alert color="primary" %}}

Пожалуйста, используйте любой из вышеупомянутых методов при запуске приложения, то есть; перед вызовом любых других объектов Aspose.Diagram API.

{{% /alert %}} {{% alert color="primary" %}}

Если для установки источников шрифта используются все вышеперечисленные методы, вступят в силу только последние настройки.

{{% /alert %}}

