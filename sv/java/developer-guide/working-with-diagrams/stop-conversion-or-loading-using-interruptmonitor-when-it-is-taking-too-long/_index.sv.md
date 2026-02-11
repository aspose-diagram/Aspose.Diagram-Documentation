---
title: Stoppa konvertering eller laddning med InterruptMonitor när det tar för lång tid
type: docs
weight: 30
url: /sv/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **Möjliga användningsscenarier**

Aspose.Diagram låter dig stoppa konverteringen av Diagram till olika format som PDF, HTML etc. med hjälp av[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) objekt när det tar för lång tid. Konverteringsprocessen är ofta både CPU- och minnesintensiv och det är ofta användbart att stoppa den när resurserna är begränsade. Du kan använda[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) både för att stoppa konverteringen och för att sluta ladda enorma diagram. Använd[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) egendom för att stoppa konvertering och[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) egendom för lastning av enorma diagram.

## **Stoppa konvertering eller laddning med InterruptMonitor när det tar för lång tid**

Följande exempelkod förklarar användningen av[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) objekt. Koden konverterar en ganska stor Visio-fil till PDF. Det tar flera sekunder (dvs.*mer än 30 sekunder*) för att få det konverterat på grund av dessa kodrader.

{{< highlight "java" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Som du ser**Enorma.vsdx** är en ganska stor VSDX-fil. Men den**StopConversionOrLoadingUsingInterruptMonitor()**metoden avbryter konverteringen efter 10 sekunder och programmet avslutas/avslutas. Använd följande kod för att köra exempelkoden.

{{< highlight "java" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Exempelkod**
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
