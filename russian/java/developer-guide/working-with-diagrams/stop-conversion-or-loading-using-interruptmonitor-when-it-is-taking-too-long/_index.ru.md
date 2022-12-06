---
title: Остановите преобразование или загрузку с помощью InterruptMonitor, если это занимает слишком много времени
type: docs
weight: 30
url: /ru/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **Возможные сценарии использования**

Aspose.Diagram позволяет остановить преобразование Diagram в различные форматы, такие как PDF, HTML и т. д., с помощью[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) объект, когда это занимает слишком много времени. Процесс преобразования часто интенсивно использует как ЦП, так и память, и часто бывает полезно остановить его, когда ресурсы ограничены. Вы можете использовать[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) как для остановки преобразования, так и для прекращения загрузки огромного diagram. Пожалуйста, используйте[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) свойство для остановки преобразования и[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) свойство для загрузки огромного diagram.

## **Остановите преобразование или загрузку с помощью InterruptMonitor, если это занимает слишком много времени**

В следующем примере кода объясняется использование[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) объект. Код преобразует довольно большой файл Visio в PDF. Это займет несколько секунд (т.е.*более 30 секунд*), чтобы преобразовать его из-за этих строк кода.

{{< highlight "java" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Как видишь**Огромный.vsdx** довольно большой файл VSDX. Тем не менее**StopConversionOrLoadingUsingInterruptMonitor()**метод прерывает преобразование через 10 секунд, и программа завершается/завершается. Пожалуйста, используйте следующий код для выполнения примера кода.

{{< highlight "java" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Образец кода**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-StopConversionOrLoadingUsingInterruptMonitor.java" >}}
