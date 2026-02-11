---
title: Остановите преобразование или загрузку с помощью InterruptMonitor, если это занимает слишком много времени
type: docs
weight: 30
url: /ru/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **Возможные сценарии использования**

Aspose.Diagram позволяет остановить преобразование Diagram в различные форматы, такие как PDF, HTML и т. д., используя[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) объект, когда это занимает слишком много времени. Процесс преобразования часто интенсивно использует как ЦП, так и память, и часто бывает полезно остановить его, когда ресурсы ограничены. Вы можете использовать[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) как для остановки преобразования, так и для прекращения загрузки огромного diagram. Пожалуйста, используйте[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) свойство для остановки преобразования и[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) свойство для загрузки огромного diagram.

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

