---
title: Stoppen Sie die Konvertierung oder das Laden mit InterruptMonitor, wenn es zu lange dauert
type: docs
weight: 30
url: /de/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **Mögliche Nutzungsszenarien**

Aspose.Diagram allows you to stop the conversion of Diagram to various formats like PDF, HTML etc. using the [**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) Objekt, wenn es zu lange dauert. Der Konvertierungsprozess ist häufig sowohl CPU- als auch speicherintensiv und es ist oft sinnvoll, ihn anzuhalten, wenn die Ressourcen begrenzt sind. Sie können verwenden[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) Sowohl zum Stoppen der Konvertierung als auch zum Stoppen des Ladens riesige diagram. Bitte verwenden[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) Eigenschaft zum Stoppen der Konvertierung und[**LoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) Grundstück zum Laden riesig diagram.

## **Stoppen Sie die Konvertierung oder das Laden mit InterruptMonitor, wenn es zu lange dauert**

Der folgende Beispielcode erläutert die Verwendung von[**InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) object. The code converts quite a large Visio file to PDF. It will take several seconds (i.e. *mehr als 30 Sekunden*), um es aufgrund dieser Codezeilen konvertieren zu lassen.

{{< highlight "java" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Wie du siehst**Riesig.vsdx** ist eine ziemlich große VSDX-Datei. Allerdings ist die**StopConversionOrLoadingUsingInterruptMonitor()**Methode unterbricht die Konvertierung nach 10 Sekunden und Programm endet/beendet. Bitte verwenden Sie den folgenden Code, um den Beispielcode auszuführen.

{{< highlight "java" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Beispielcode**

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

