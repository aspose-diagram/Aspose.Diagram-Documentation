---
title: أوقف التحويل أو التحميل باستخدام InterruptMonitor عندما يستغرق وقتًا طويلاً
type: docs
weight: 30
url: /ar/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **سيناريوهات الاستخدام الممكنة**

يسمح لك Aspose.Diagram بإيقاف تحويل Diagram إلى تنسيقات مختلفة مثل PDF و HTML وما إلى ذلك باستخدام[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) كائن عندما يستغرق وقتا طويلا. غالبًا ما تكون عملية التحويل كثيفة الاستخدام لوحدة المعالجة المركزية والذاكرة وغالبًا ما يكون من المفيد إيقافها عندما تكون الموارد محدودة. يمكنك استخدام[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) كلا لإيقاف التحويل وكذلك لإيقاف التحميل الضخم diagram. الرجاء استخدام[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) خاصية وقف التحويل و[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) عقار للتحميل ضخمة diagram.

## **أوقف التحويل أو التحميل باستخدام InterruptMonitor عندما يستغرق وقتًا طويلاً**

يشرح نموذج التعليمات البرمجية التالي استخدام[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) هدف. يقوم الكود بتحويل ملف Visio كبير جدًا إلى ملف PDF. سيستغرق الأمر عدة ثوانٍ (على سبيل المثال*أكثر من 30 ثانية*) لتحويلها بسبب هذه الأسطر من التعليمات البرمجية.

{{< highlight "java" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 كما ترى**ضخم vsdx** هو ملف VSDX ضخم جدًا. ومع ذلك ، فإن**StopConversionOrLoadingUsingInterruptMonitor ()**الطريقة تقاطع التحويل بعد 10 ثوانٍ وينتهي البرنامج / ينتهي. الرجاء استخدام التعليمات البرمجية التالية لتنفيذ نموذج التعليمات البرمجية.

{{< highlight "java" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **عينة من الرموز**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-StopConversionOrLoadingUsingInterruptMonitor.java" >}}
