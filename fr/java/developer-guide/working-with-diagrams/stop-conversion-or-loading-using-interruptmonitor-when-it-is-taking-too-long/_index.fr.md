---
title: Arrêtez la conversion ou le chargement à l'aide d'InterruptMonitor lorsque cela prend trop de temps
type: docs
weight: 30
url: /fr/java/stop-conversion-or-loading-using-interruptmonitor-when-it-is-taking-too-long/
---
## **Scénarios d'utilisation possibles**

Aspose.Diagram allows you to stop the conversion of Diagram to various formats like PDF, HTML etc. using the [**Moniteur d'interruption**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) objet quand cela prend trop de temps. Le processus de conversion est souvent gourmand en CPU et en mémoire et il est souvent utile de l'arrêter lorsque les ressources sont limitées. Vous pouvez utiliser[**Moniteur d'interruption**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) à la fois pour arrêter la conversion et pour arrêter le chargement de l'énorme diagram. Veuillez utiliser[**Diagram.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) propriété d'arrêter la conversion et[**LoadOptions.InterruptMonitorLoadOptions.InterruptMonitor**](https://reference.aspose.com/diagram/java/com.aspose.diagram/loadoptions#InterruptMonitor) propriété pour le chargement énorme diagram.

## **Arrêtez la conversion ou le chargement à l'aide d'InterruptMonitor lorsque cela prend trop de temps**

L'exemple de code suivant explique l'utilisation de[**Moniteur d'interruption**](https://reference.aspose.com/diagram/java/com.aspose.diagram/InterruptMonitor) object. The code converts quite a large Visio file to PDF. It will take several seconds (i.e. *plus de 30 secondes*) pour le convertir à cause de ces lignes de code.

{{< highlight "java" >}}

	      Aspose.Diagram.LoadOptions o = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
	      o.InterruptMonitor = im;
	      Diagram diagram = new Diagram("Huge.vsdx", o);

{{< /highlight >}}

 Comme tu vois**énorme.vsdx** est un fichier VSDX assez énorme. Cependant, le**StopConversionOrLoadingUsingInterruptMonitor()**La méthode interrompt la conversion après 10 secondes et le programme se termine/se termine. Veuillez utiliser le code suivant pour exécuter l'exemple de code.

{{< highlight "java" >}}

 new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

{{< /highlight >}}

## **Exemple de code**

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

