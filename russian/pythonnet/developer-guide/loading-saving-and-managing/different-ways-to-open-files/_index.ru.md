---
title: Различные способы открытия файлов
type: docs
weight: 10
url: /ru/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

С Aspose.Diagram легко открывать файлы, например, для получения данных или использовать шаблон конструктора для ускорения процесса разработки.

{{% /alert %}}

## **Открытие файла via Путь**

 Разработчики могут открыть файл Microsoft Diagram, используя его путь к файлу на локальном компьютере, указав его в**Diagram**конструктор класса. Просто передайте путь в конструкторе как*нить*. Aspose.Diagram автоматически определит тип формата файла.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaPath.py" >}}

## **Открытие файла via в потоке**

 Также просто открыть файл Visio в виде потока. Для этого используйте перегруженную версию конструктора, который принимает*BufferStream*объект, содержащий файл.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaStream.py" >}}

## **Открытие файла с помощью LoadOptions**

 Чтобы открыть файл с параметрами загрузки, используйте команду**Параметры загрузки**классы, чтобы установить соответствующие параметры классов для загружаемого файла шаблона.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaLoadOptions.py" >}}

