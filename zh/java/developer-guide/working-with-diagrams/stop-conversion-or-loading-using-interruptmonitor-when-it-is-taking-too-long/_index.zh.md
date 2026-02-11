---
title: 当时间过长时使用 InterruptMonitor 停止转换或加载
type: docs
weight: 30
url: /zh/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **可能的使用场景**

Aspose.Diagram allows you to stop the conversion of Diagram to various formats like PDF, HTML etc. using the [**中断监视器**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor)反对时间太长。转换过程通常是 CPU 和内存密集型的，当资源有限时停止它通常很有用。您可以使用[**中断监视器**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor)既用于停止转换也用于停止加载巨大的 diagram。请使用[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor)停止转换的属性和[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor)用于加载巨大 diagram 的属性。

## **当时间过长时使用 InterruptMonitor 停止转换或加载**

下面的示例代码解释了[**中断监视器**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) object. The code converts quite a large Visio file to PDF. It will take several seconds (i.e. *超过 30 秒*因为这些代码行而将其转换。

{{< highlight "java" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

正如你看到的**巨大.vsdx**是一个非常大的 VSDX 文件。但是，那**StopConversionOrLoadingUsingInterruptMonitor()**方法在 10 秒后中断转换，程序结束/终止。请使用以下代码来执行示例代码。

{{< highlight "java" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **示例代码**
```
{{< highlight "java" >}}
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
```
