---
title: أوقف التحويل أو التحميل باستخدام InterruptMonitor عندما يستغرق وقتًا طويلاً
type: docs
weight: 30
url: /ar/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **سيناريوهات الاستخدام الممكنة**

يسمح لك Aspose.Diagram بإيقاف تحويل Diagram إلى تنسيقات مختلفة مثل PDF و HTML وما إلى ذلك باستخدام[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) كائن عندما يستغرق وقتا طويلا. غالبًا ما تكون عملية التحويل كثيفة الاستخدام لوحدة المعالجة المركزية والذاكرة وغالبًا ما يكون من المفيد إيقافها عندما تكون الموارد محدودة. يمكنك استخدام[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) كلا لإيقاف التحويل وكذلك لإيقاف التحميل الضخم diagram. الرجاء استخدام[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) خاصية وقف التحويل و[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) عقار للتحميل ضخمة diagram.

## **أوقف التحويل أو التحميل باستخدام InterruptMonitor عندما يستغرق وقتًا طويلاً**

يشرح نموذج التعليمات البرمجية التالي استخدام[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) هدف. يقوم الكود بتحويل ملف Visio كبير جدًا إلى PDF. سيستغرق الأمر عدة ثوانٍ (على سبيل المثال*أكثر من 30 ثانية*) لتحويلها بسبب هذه الأسطر من التعليمات البرمجية.

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

{{< highlight java >}}
import com.aspose.diagram.Diagram;
import com.aspose.diagram.InterruptMonitor;
import com.aspose.diagram.SaveFileFormat;

public class StopConversionOrLoadingUsingInterruptMonitor
{
	
	//Create InterruptMonitor object
    InterruptMonitor im = new InterruptMonitor();

    public class ThreadStart extends Thread
	{	
		private int ThreadFunc;
		
		public ThreadStart(int threadFunc)
		{
			this.ThreadFunc = threadFunc;
		}
        
        //This function will create diagram and convert it to Pdf format
        void CreateDiagramAndConvertItToPdfFormat() throws Exception
        {
            //Create a diagram object
            Diagram diagram = new Diagram("huge.vsdx");

            //Assign it InterruptMonitor object
            diagram.setInterruptMonitor(im);

            try
            {
                //Save the workbook to Pdf format
                diagram.save( "output_InterruptMonitor.pdf",SaveFileFormat.PDF);
                
                //Show successful message
                System.out.println("Diagram to PDF - Successful Conversion");
            }
            catch (Exception ex)
            {
                System.out.println("Diagram process Interrupted - Message: " + ex.getMessage());
            }
        }
        
        //This function will interrupt the conversion process after 10s
        void WaitForWhileAndThenInterrupt() throws Exception
        {
            Thread.sleep(1000 * 10);
            im.interrupt();
        }
        
        public void run() 
        {
        	try
        	{
        		if(this.ThreadFunc == 1)
        		{
        			CreateDiagramAndConvertItToPdfFormat();
        		}
            	
            	if(this.ThreadFunc == 2)
            	{
            		WaitForWhileAndThenInterrupt();
            	}
        		
        	}
        	catch(Exception ex)
        	{
        		System.out.println("Process Interrupted - Message: " + ex.getMessage());
        	}
        	
        }
	}//ThreadStart

    public void TestRun() throws Exception
	{
		ThreadStart t1 = new ThreadStart(1);
		ThreadStart t2 = new ThreadStart(2);
		
		t1.start();
		t2.start();
		
		t1.join();
		t2.join();
	}
	    public static void main(String[] args) throws Exception {

		new StopConversionOrLoadingUsingInterruptMonitor().TestRun();
		
		// Print the message
		System.out.println("StopConversionOrLoadingUsingInterruptMonitor executed successfully.");
	}
}
{{< /highlight >}}

