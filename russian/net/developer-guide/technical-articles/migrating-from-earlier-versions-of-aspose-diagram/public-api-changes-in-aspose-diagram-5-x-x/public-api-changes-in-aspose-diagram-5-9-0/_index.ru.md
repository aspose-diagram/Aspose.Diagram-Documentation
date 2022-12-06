---
title: Общедоступный API Изменения в Aspose.Diagram 5.9.0
type: docs
weight: 10
url: /ru/net/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 5.8.0 до 5.9.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
## **Сохранить результирующий HTML в поток**
В класс Diagram добавлен новый метод Save. Он принимает два параметра: объект потока и формат сохраняемого файла.
Пример кода:

**C#**

{{< highlight "java" >}}

 // load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);

{{< /highlight >}}

**ВБ**

{{< highlight "java" >}}

 ' load an existing visio diagram

Dim diagram As Diagram = New Diagram("Basic Flowchart.vsd")

' save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream()

diagram.Save(stream, SaveFileFormat.HTML)

{{< /highlight >}}
## **Скопируйте темы и PageSheet из другого Visio**
Класс Diagram предлагает метод CopyTheme, а класс PageSheet предлагает метод Copy для достижения цели копирования фигуры и других задач манипулирования.
 Примеры кодов:[Копирование фигур из существующей Visio](/diagram/ru/net/add-retrieve-copy-and-read-visio-shape-data/)
## **VSTX и VSSX Параметры сохранения добавлены в SaveFileFormat.**
Раньше Aspose.Diagram API поддерживал чтение и запись в формате VSDX, но теперь мы добавили поддержку записи диаграмм и в форматах VSTX и VSSX. Примеры кодов:

**C#**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}

**ВБ**

{{< highlight "java" >}}

 ' save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX)

' save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX)

{{< /highlight >}}
## **VSSX Параметр чтения добавлен в LoadFileFormat**
Ранее Aspose.Diagram API поддерживал чтение и запись в формате VSDX, но теперь мы также добавили поддержку чтения в формате трафарета VSSX. Примеры кодов:

**C#**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}

**ВБ**

{{< highlight "java" >}}

 ' read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX)

{{< /highlight >}}
