---
title: Загрузите и настройте Aspose.Diagram в PHP
type: docs
weight: 10
url: /ru/java/download-and-configure-aspose-diagram-in-php/
---
## **Скачать необходимые библиотеки**
Загрузите необходимые библиотеки, указанные ниже. Они необходимы для выполнения Aspose.Diagram Java для примеров Ruby.

- [Aspose.Diagram for Java Компонент](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram)
## **Загрузите примеры с сайтов социального кодирования**
Следующие выпуски работающих примеров доступны для загрузки на указанных ниже сайтах социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/tree/master/Plugins/Aspose_Diagram_Java_for_PHP)
## **Установка**
Установить Aspose.Diagram Java для PHP очень просто и легко, следуйте инструкциям:

Запустите следующую команду.

{{< highlight "java" >}}

 $ gem install asposediagramjava

{{< /highlight >}}
## **С использованием**
Включите необходимые файлы для экспорта чертежа visio в документ PDF.

{{< highlight "java" >}}

 require File.dirname(File.dirname(File.dirname(__FILE__))) + '/lib/asposediagramjava'

include Asposediagramjava

include Asposediagramjava::ExportToPdf

initialize_aspose_Diagram

{{< /highlight >}}

Давайте разберемся с приведенным выше кодом.

1. Первая строка гарантирует, что Aspose.Diagram загружен и доступен.
1. Включите файлы, необходимые для доступа к Aspose.Diagram
1. Инициализируйте библиотеки. Классы aspose Java загружаются по пути, указанному в файле aspose.yml.
