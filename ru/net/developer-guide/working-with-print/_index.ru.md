---
title: Работа с печатью
type: docs
weight: 80
url: /ru/net/working-with-print/
description: В этом разделе объясняется, как распечатать документ XpsPrint via с номером Aspose.Diagram.
---
## **Как распечатать документ на сервере via XpsPrint API**
Эта статья может быть полезна всем, кто хочет отправить документ XPS на неуправляемый принтер XpsPrint API из приложения .NET. Но главная цель этой статьи — показать, как распечатать diagram из сервисного приложения ASP.NET или Windows, используя Aspose.Diagram и XpsPrint API.
### **Проблема**
При разработке приложения .NET и необходимости его вывода на печать можно использовать классы в пространстве имен System.Drawing.Printing или классы WPF. Но, как выясняется, если вы разрабатываете сервисное приложение ASP.NET или Windows, ваши возможности для печати сильно ограничены, потому что Microsoft не рекомендует использовать эти подходы. См. приведенные ниже ссылки для получения дополнительной информации.

<http://support.microsoft.com/kb/324565>

Использование классов печати .NET Framework не поддерживается службой. Сюда входят страницы ASP, которые обычно запускаются в контексте службы сервера.

<http://msdn.microsoft.com/en-us/library/system.drawing.printing.aspx>

Классы в пространстве имен System.Drawing.Printing не поддерживаются для использования в службе Windows или приложении или службе ASP.NET. Попытка использовать эти классы из одного из этих типов приложений может привести к непредвиденным проблемам, таким как снижение производительности службы и исключения во время выполнения.

<http://msdn.microsoft.com/en-us/library/bb613549.aspx>

Использование WPF для создания служб Windows не поддерживается. Поскольку WPF — это технология представления, службе Windows требуются соответствующие разрешения для выполнения визуальных операций, требующих взаимодействия с пользователем. Если служба Windows не имеет соответствующих разрешений, могут быть неожиданные результаты.

Объект Document предоставляет семейство методов Print для печати документов, и эти методы печатают via классы печати, определенные в пространстве имен System.Drawing.Printing. Есть много клиентов Aspose.Diagram, которые без проблем используют этот метод печати в своих серверных приложениях, но есть способ выполнить рекомендации Microsoft, и он описан в этой статье.
### **Решение**
Правильным способом печати документов в соответствии с Microsoft является использование неуправляемого XpsPrint API. Этот API доступен на Windows 7, Windows Server 2008 R2, а также на Windows Vista, если установлено обновление платформы для Windows Vista.

Поскольку Aspose.Diagram может легко преобразовать любой документ в XPS, нам нужно только написать код, который передает документ XPS в XpsPrint API. Единственная проблема заключается в том, что XpsPrint API неуправляемый и требует некоторых знаний о вызове платформы.
### **Код**
Мы создали класс XpsPrintHelper с методом Print, который очень прост в использовании. Вам просто нужно указать документ, который вы хотите напечатать, имя принтера и необязательное имя задания. Если возникла проблема с отправкой или печатью документа, метод выдаст исключение.

Последний параметр — это логическое значение, указывающее, должен ли код ждать, пока задание не будет напечатано, или возвращаться сразу после отправки задания на печать. Если вы решите вернуться немедленно, то вы не сможете определить, успешно распечатался документ в итоге или нет.
#### **Образец программирования**
В следующем примере кода показано, как вызвать служебный класс для печати via XPS.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
// Specify the name of the printer you want to print to.
const string printerName = @"\\COMPANY\Brother MFC-885CW Printer";

// Print the document.
XpsPrintHelper.Print(diagram, printerName, "My Test Job", true);

{{< /highlight >}}



Существует две перегрузки метода XpsPrintHelper.Print. Первая перегрузка принимает объект Aspose.Diagram.Diagram и сохраняет его в MemoryStream в формате XPS. Затем он вызывает другую перегрузку XpsPrintHelper.Print.

Если вы хотите использовать этот образец без Aspose.Diagram (например, у вас уже есть документ XPS и вы просто хотите распечатать его из приложения службы ASP.NET или Windows), вы можете просто удалить этот метод.
#### **XPS Пример программирования потоковой передачи и печати**
Этот пример кода преобразует Diagram в поток XPS и печатает.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
/// <summary>
/// Sends an Aspose.Diagram document to a printer using the XpsPrint API.
/// </summary>
/// <param name="diagram"></param>
/// <param name="printerName"></param>
/// <param name="jobName">Job name. Can be null.</param>
/// <param name="isWait">True to wait for the job to complete. False to return immediately after submitting the job.</param>
/// <exception cref="Exception">Thrown if any error occurs.</exception>
public static void Print(Diagram diagram, string printerName, string jobName, bool isWait)
{
    if (diagram == null)
        throw new ArgumentNullException("document");

    // Use Aspose.Diagram to convert the document to XPS and store in a memory stream.
    MemoryStream stream = new MemoryStream();
    diagram.Save(stream, SaveFileFormat.XPS);
    stream.Position = 0;

    Print(stream, printerName, jobName, isWait);
}

{{< /highlight >}}



Вторая перегрузка XpsPrintHelper.Print принимает объект Stream. Поток должен содержать документ в формате XPS. Этот метод запускает задание печати XPS, отправляет документ на XpsPrint API, а затем при необходимости ожидает результата.
#### **XpsPrint API Образец программирования**
В этом примере кода документ XPS печатается с использованием XpsPrint API.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
/// <summary>
/// Sends a stream that contains a document in the XPS format to a printer using the XpsPrint API.
/// Has no dependency on Aspose.Diagram, can be used in any project.
/// </summary>
/// <param name="stream"></param>
/// <param name="printerName"></param>
/// <param name="jobName">Job name. Can be null.</param>
/// <param name="isWait">True to wait for the job to complete. False to return immediately after submitting the job.</param>
/// <exception cref="Exception">Thrown if any error occurs.</exception>
public static void Print(Stream stream, string printerName, string jobName, bool isWait)
{
    if (stream == null)
        throw new ArgumentNullException("stream");
    if (printerName == null)
        throw new ArgumentNullException("printerName");

    // Create an event that we will wait on until the job is complete.
    IntPtr completionEvent = CreateEvent(IntPtr.Zero, true, false, null);
    if (completionEvent == IntPtr.Zero)
        throw new Win32Exception();

    try
    {
        IXpsPrintJob job;
        IXpsPrintJobStream jobStream;
        StartJob(printerName, jobName, completionEvent, out job, out jobStream);

        CopyJob(stream, job, jobStream);

        if (isWait)
        {
            WaitForJob(completionEvent);
            CheckJobStatus(job);
        }
    }
    finally
    {
        if (completionEvent != IntPtr.Zero)
            CloseHandle(completionEvent);
    }
}

{{< /highlight >}}



Код для методов StartJob, CopyJob, WaitForJob и CheckJobStatus, а также определения интерфейсов IXpsPrintJob и IXpsPrintJobStream довольно низкоуровневый и использует Platform Invoke и COM Interop. Этот код не включен в статью для краткости, но доступен в загружаемом образце.

XpsPrint API также предоставляет дополнительные функции, такие как отслеживание хода выполнения задания, но наш XpsPrintHelper представляет собой очень простую оболочку и не предоставляет эту функцию. Вы можете добавить это сами, если хотите.

{{% alert color="primary" %}}

Когда вы запускаете проект, он печатает образец документа на указанном принтере. Чтобы сделать результаты видимыми, открывается окно консоли. Программа отображает сообщение об успешном выполнении или текст исключения, если оно было создано.

{{% /alert %}}
## **Печать Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) предоставляет четыре метода перегрузки для печати диаграмм. Эти методы достаточно гибкие, чтобы распечатать diagram на принтере по умолчанию или на любом доступном принтере с индивидуальными настройками. Вам нужно только выбрать подходящий метод печати в соответствии с требованиями.
### **Печать на принтер по умолчанию**
Печать diagram на принтере по умолчанию довольно проста в Aspose.Diagram for .NET. Выполните следующие шаги, чтобы напечатать diagram на принтере по умолчанию:

- Создайте экземпляр класса Diagram для загрузки diagram, который должен быть напечатан.
- Вызовите метод Print без параметров, предоставляемых объектом Diagram.
#### **Пример программирования печати на принтере по умолчанию**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the default printer
diagram.Print();

{{< /highlight >}}

### **Печать на указанный принтер**
Для печати diagram на конкретном принтере требуется имя принтера в качестве параметра метода печати Diagram. Выполните следующие шаги, чтобы напечатать diagram на нужном принтере:

- Создайте экземпляр класса Diagram для загрузки diagram, который должен быть напечатан.
- Вызовите метод Print класса Diagram с именем принтера в качестве строкового параметра для метода Print.
#### **Пример программирования печати на конкретном принтере**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the printer name
diagram.Print("LaserJet1100");

{{< /highlight >}}

### **Установка имени принтера и документа**
Aspose.Diagram API позволяет задать конкретный принтер и имя документа для задания на печать. Выполните следующие шаги, чтобы распечатать diagram на нужном принтере:

- Создайте экземпляр класса Diagram для загрузки diagram, который должен быть напечатан.
- Вызовите метод Print класса Diagram с принтером и именем документа в качестве строкового параметра для метода Print.
#### **Пример программирования установки имени принтера и документа**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.Print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}

