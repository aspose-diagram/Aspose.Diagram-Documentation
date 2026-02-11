---
title: Остановите преобразование или загрузку с помощью InterruptMonitor, если это занимает слишком много времени
type: docs
weight: 30
url: /ru/net/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
description: В этом разделе объясняется, как остановить преобразование или загрузку с помощью Aspose.Diagram.
---
## **Возможные сценарии использования**

Aspose.Diagram позволяет остановить преобразование Diagram в различные форматы, такие как PDF, HTML и т. д., используя[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) объект, когда это занимает слишком много времени. Процесс преобразования часто интенсивно использует как ЦП, так и память, и часто бывает полезно остановить его, когда ресурсы ограничены. Вы можете использовать[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) как для остановки преобразования, так и для прекращения загрузки огромного diagram. Пожалуйста, используйте[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/interruptmonitor) свойство для остановки преобразования и[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/loadoptions/properties/interruptmonitor) свойство для загрузки огромного diagram.

## **Остановите преобразование или загрузку с помощью InterruptMonitor, если это занимает слишком много времени**

В следующем примере кода объясняется использование[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) объект. Код преобразует довольно большой файл Visio в PDF. Это займет несколько секунд (т.е.*более 30 секунд*), чтобы преобразовать его из-за этих строк кода.

{{< highlight "csharp" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Как видишь**Огромный.vsdx** довольно большой файл VSDX. Тем не менее**Ждать для пока и потом прерывать ()**метод прерывает преобразование через 1 секунду, и программа завершается/завершается. Пожалуйста, используйте следующий код для выполнения примера кода.

{{< highlight "csharp" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Образец кода**

{{< highlight csharp >}}
static string outputDir = RunExamples.Get_OutputDirectory();

//Create InterruptMonitor object
InterruptMonitor im = new InterruptMonitor();

//This function will load diagram
void loadDiagram()
{
    try
	  {
	
	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

	  }
	  catch(Exception e)
	  {
	      Console.WriteLine("Diagram Process Interrupted - Message: " + e.Message);
	  }

}

//This function will interrupt the conversion process after 1s
void WaitForWhileAndThenInterrupt()
{
    Thread.Sleep(1000 * 1);
    im.Interrupt();
}

public void TestRun()
{
    ThreadStart ts1 = new ThreadStart(this.loadDiagram);
    Thread t1 = new Thread(ts1);
    t1.Start();

    ThreadStart ts2 = new ThreadStart(this.WaitForWhileAndThenInterrupt);
    Thread t2 = new Thread(ts2);
    t2.Start();

    t1.Join();
    t2.Join();
}


public static void Run()
{
    new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

    Console.WriteLine("Interrupt successfully.");
}
{{< /highlight >}}

