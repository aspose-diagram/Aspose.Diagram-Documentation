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
