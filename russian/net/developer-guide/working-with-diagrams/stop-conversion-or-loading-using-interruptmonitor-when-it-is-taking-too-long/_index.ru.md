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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Interrupt-Interrupt-StopConversionOrLoadingUsingInterruptMonitor.cs" >}}
