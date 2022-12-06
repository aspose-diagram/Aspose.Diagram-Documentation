---
title: Çok uzun sürdüğünde InterruptMonitor kullanarak dönüştürmeyi veya yüklemeyi durdurun
type: docs
weight: 30
url: /tr/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **Olası Kullanım Senaryoları**

Aspose.Diagram, Diagram'in PDF, HTML gibi çeşitli biçimlere dönüştürülmesini durdurmanıza olanak tanır.[**Kesinti İzleme**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) çok uzun sürdüğünde itiraz edin. Dönüştürme işlemi genellikle hem CPU hem de Bellek açısından yoğundur ve kaynaklar sınırlı olduğunda genellikle işlemi durdurmak yararlıdır. Kullanabilirsiniz[**Kesinti İzleme**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) hem dönüştürmeyi durdurmak hem de büyük diagram yüklemesini durdurmak için. Lütfen kullanın[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) dönüştürmeyi durdurma özelliği ve[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) büyük yükleme özelliği diagram.

## **Çok uzun sürdüğünde InterruptMonitor kullanarak dönüştürmeyi veya yüklemeyi durdurun**

Aşağıdaki örnek kod, kullanımını açıklar[**Kesinti İzleme**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) nesne. Kod oldukça büyük bir Visio dosyasını PDF'e dönüştürür. Birkaç saniye sürecektir (örn.*30 saniyeden fazla*) bu kod satırları nedeniyle dönüştürülmesini sağlamak için.

{{< highlight "java" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Gördüğünüz gibi**Çok büyük.vsdx** oldukça büyük bir VSDX dosyasıdır. Ancak**StopConversionOrLoadingUsingInterruptMonitor()**yöntemi, dönüştürmeyi 10 saniye sonra keser ve program biter/sonlanır. Lütfen örnek kodu çalıştırmak için aşağıdaki kodu kullanın.

{{< highlight "java" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Basit kod**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-StopConversionOrLoadingUsingInterruptMonitor.java" >}}
