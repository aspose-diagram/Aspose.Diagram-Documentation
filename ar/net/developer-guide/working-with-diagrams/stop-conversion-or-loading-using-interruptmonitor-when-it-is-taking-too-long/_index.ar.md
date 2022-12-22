---
title: أوقف التحويل أو التحميل باستخدام InterruptMonitor عندما يستغرق وقتًا طويلاً
type: docs
weight: 30
url: /ar/net/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
description: يوضح هذا القسم كيفية إيقاف التحويل أو التحميل باستخدام Aspose.Diagram.
---
## **سيناريوهات الاستخدام الممكنة**

يسمح لك Aspose.Diagram بإيقاف تحويل Diagram إلى تنسيقات مختلفة مثل PDF و HTML وما إلى ذلك باستخدام[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) كائن عندما يستغرق وقتا طويلا. غالبًا ما تكون عملية التحويل كثيفة الاستخدام لوحدة المعالجة المركزية والذاكرة وغالبًا ما يكون من المفيد إيقافها عندما تكون الموارد محدودة. يمكنك استخدام[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) كلا لإيقاف التحويل وكذلك لإيقاف التحميل الضخم diagram. الرجاء استخدام[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/interruptmonitor) خاصية وقف التحويل و[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/loadoptions/properties/interruptmonitor) عقار للتحميل ضخمة diagram.

## **أوقف التحويل أو التحميل باستخدام InterruptMonitor عندما يستغرق وقتًا طويلاً**

يشرح نموذج التعليمات البرمجية التالي استخدام[**InterruptMonitor**](https://reference.aspose.com/diagram/net/aspose.diagram/interruptmonitor) هدف. يقوم الكود بتحويل ملف Visio كبير جدًا إلى PDF. سيستغرق الأمر عدة ثوانٍ (على سبيل المثال*أكثر من 30 ثانية*) لتحويلها بسبب هذه الأسطر من التعليمات البرمجية.

{{< highlight "csharp" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 كما ترى**ضخم vsdx** هو ملف VSDX ضخم جدًا. ومع ذلك ، فإن**WaitForWhileAndThenInterrupt ()**الطريقة تقاطع التحويل بعد ثانية واحدة وينتهي البرنامج / ينتهي. الرجاء استخدام التعليمات البرمجية التالية لتنفيذ نموذج التعليمات البرمجية.

{{< highlight "csharp" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **عينة من الرموز**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Interrupt-Interrupt-StopConversionOrLoadingUsingInterruptMonitor.cs" >}}
