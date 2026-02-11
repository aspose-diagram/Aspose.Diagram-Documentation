---
title: Çok uzun sürdüğünde InterruptMonitor kullanarak dönüştürmeyi veya yüklemeyi durdurun
type: docs
weight: 30
url: /tr/net/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
description: Bu bölüm, Aspose.Diagram ile dönüştürmenin veya yüklemenin nasıl durdurulacağını açıklar.
---
## **Olası Kullanım Senaryoları**

Aspose.Diagram, Diagram'in PDF, HTML gibi çeşitli biçimlere dönüştürülmesini durdurmanıza olanak tanır.[**Kesinti İzleme**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) çok uzun sürdüğünde itiraz edin. Dönüştürme işlemi genellikle hem CPU hem de Bellek açısından yoğundur ve kaynaklar sınırlı olduğunda genellikle işlemi durdurmak yararlıdır. Kullanabilirsiniz[**Kesinti İzleme**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) hem dönüştürmeyi durdurmak hem de büyük diagram yüklemesini durdurmak için. Lütfen kullanın[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/interruptmonitor) dönüştürmeyi durdurma özelliği ve[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/loadoptions/properties/interruptmonitor) büyük yükleme özelliği diagram.

## **Çok uzun sürdüğünde InterruptMonitor kullanarak dönüştürmeyi veya yüklemeyi durdurun**

Aşağıdaki örnek kod, kullanımını açıklar[**Kesinti İzleme**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) nesne. Kod oldukça büyük bir Visio dosyasını PDF'e dönüştürür. Birkaç saniye sürecektir (örn.*30 saniyeden fazla*) bu kod satırları nedeniyle dönüştürülmesini sağlamak için.

{{< highlight "csharp" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Gördüğünüz gibi**Çok büyük.vsdx** oldukça büyük bir VSDX dosyasıdır. Ancak**WaitForWhileAndThenInterrupt()**yöntemi 1 saniye sonra dönüştürmeyi keser ve program biter/sonlanır. Lütfen örnek kodu çalıştırmak için aşağıdaki kodu kullanın.

{{< highlight "csharp" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Basit kod**

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

