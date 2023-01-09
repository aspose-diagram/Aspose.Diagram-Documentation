---
title: Общедоступный API Изменения в Aspose.Diagram 5.9.0
type: docs
weight: 10
url: /ru/java/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 5.8.0 до 5.9.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
### **Сохранить результат HTML в поток**
В класс Diagram добавлен новый метод сохранения. Он принимает два параметра: объект потока и формат сохраняемого файла.
Пример кода:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

ByteArrayOutputStream dstStream = new ByteArrayOutputStream();

diagram.save(dstStream, SaveFileFormat.HTML);

// In you want to read the result into a Diagram object again, in Java you need to get the

// data bytes and wrap into an input stream.

ByteArrayInputStream srcStream = new ByteArrayInputStream(dstStream.toByteArray());

{{< /highlight >}}
### **Скопируйте темы и PageSheet из другого Visio**
Класс Diagram предлагает метод CopyTheme, а класс PageSheet предлагает метод Copy для достижения цели копирования фигуры и других задач манипулирования.
 Примеры кодов:[Копирование фигур из существующей Visio](/diagram/ru/java/working-with-visio-shape-data/#copy-shapes-from-an-existing-visio)
### **VSTX и VSSX Параметры сохранения добавлены в SaveFileFormat.**
Раньше Aspose.Diagram API поддерживал чтение и запись в формате VSDX, но теперь мы добавили поддержку записи диаграмм и в форматах VSTX и VSSX. Примеры кодов:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}
### **VSSX Параметр чтения добавлен в LoadFileFormat**
Ранее Aspose.Diagram API поддерживал чтение и запись в формате VSDX, но теперь мы также добавили поддержку чтения в формате трафарета VSSX. Примеры кодов:

**Java**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram("C:\\temp\\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}
