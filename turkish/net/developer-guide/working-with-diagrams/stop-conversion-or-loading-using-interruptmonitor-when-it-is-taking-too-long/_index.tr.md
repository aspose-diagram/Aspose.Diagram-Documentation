---
title: Çok uzun sürdüğünde InterruptMonitor kullanarak dönüştürmeyi veya yüklemeyi durdurun
type: docs
weight: 30
url: /tr/net/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
description: Bu bölüm, Aspose.Diagram ile dönüştürmenin veya yüklemenin nasıl durdurulacağını açıklar.
---
## **Olası Kullanım Senaryoları**

Aspose.Diagram, Diagram'in PDF, HTML vb. gibi çeşitli biçimlere dönüştürülmesini durdurmanıza olanak tanır.[**Kesinti İzleme**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) çok uzun sürdüğünde itiraz edin. Dönüştürme işlemi genellikle hem CPU hem de Bellek açısından yoğundur ve kaynaklar sınırlı olduğunda genellikle işlemi durdurmak yararlıdır. Kullanabilirsiniz[**Kesinti İzleme**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) hem dönüştürmeyi durdurmak hem de büyük diagram yüklemesini durdurmak için. Lütfen kullanın[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/interruptmonitor) dönüştürmeyi durdurma özelliği ve[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/loadoptions/properties/interruptmonitor) büyük yükleme özelliği diagram.

## **Çok uzun sürdüğünde InterruptMonitor kullanarak dönüştürmeyi veya yüklemeyi durdurun**

Aşağıdaki örnek kod, kullanımını açıklar[**Kesinti İzleme**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) nesne. Kod, oldukça büyük bir Visio dosyasını PDF'ye dönüştürür. Birkaç saniye sürecektir (örn.*30 saniyeden fazla*) bu kod satırları nedeniyle dönüştürülmesini sağlamak için.

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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Interrupt-Interrupt-StopConversionOrLoadingUsingInterruptMonitor.cs" >}}
