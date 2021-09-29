---
title: Working with Print
type: docs
weight: 80
url: /net/working-with-print/
---

## **How to Print a Document on a Server via the XpsPrint API**
This article can be useful to anyone who wants to submit an XPS document to the unmanaged XpsPrint API from a .NET application. But the main goal if this article is to show how to print a diagram from an ASP.NET or Windows Service application using Aspose.Diagram and the XpsPrint API.
### **Problem**
When you develop a .NET application and you need to produce some printed output, you can use the classes in the System.Drawing.Printing namespace or the WPF classes. But, as it turns out, if you develop an ASP.NET or Windows Service application, then your options for printing are severely limited, because Microsoft recommends against using these approaches. See the links below for more information.

<http://support.microsoft.com/kb/324565>

The use of the .NET Framework Printing classes is not supported from a service. This includes ASP pages, which generally run in the context of the server service.

<http://msdn.microsoft.com/en-us/library/system.drawing.printing.aspx>

Classes within the System.Drawing.Printing namespace are not supported for use within a Windows service or ASP.NET application or service. Attempting to use these classes from within one of these application types may produce unexpected problems, such as diminished service performance and run-time exceptions.

<http://msdn.microsoft.com/en-us/library/bb613549.aspx>

The use of WPF to build Windows services is unsupported. Because WPF is a presentation technology, the Windows service requires the appropriate permissions to perform visual operations that involve user interaction. If the Windows service does not have the appropriate permissions, there may be unexpected results.

The Document object provides a family of the Print methods to print documents and these methods print via the .NET printing classes defined in the System.Drawing.Printing namespace. There are many customers of Aspose.Diagram who use this printing method in their server-side applications without any problems, but there is a way to comply with Microsoft’s recommendations and it is described in this article.
### **Solution**
The proper way to print documents according to Microsoft is to use the unmanaged XpsPrint API. This API is available on Windows 7, Windows Server 2008 R2 and also on Windows Vista, provided the Platform Update for Windows Vista is installed.

Since Aspose.Diagram can easily convert any document to XPS, we only need to write code that passes an XPS document to the XpsPrint API. The only problem is that the XpsPrint API is unmanaged and it requires some knowledge of the Platform Invoke.
### **The Code**
We have created the XpsPrintHelper class with the Print method, which is very easy to use. You just need to specify a document that you want to print, a printer name and an optional job name. If there was any problem submitting or printing the document, the method will throw an exception.

The last parameter is a Boolean value that specifies whether the code should wait until the job is printed or return immediately after the print job has been submitted. If you choose to return immediately, then you will not be able to determine whether the document has printed successfully or not in the end.
#### **Programming Sample**
The following code example shows how to invoke the utility class to print via XPS.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-PrintDiagramVisXPSPrinterAPI-PrintDiagramVisXPSPrinterAPI.cs" >}}


There are two overloads of the XpsPrintHelper.Print method. The first overload takes an Aspose.Diagram.Diagram object and saves it into a MemoryStream in the XPS format. Then it invokes the other XpsPrintHelper.Print overload.

If you want to use this sample without Aspose.Diagram (e.g. you already have an XPS document and just want to print it from an ASP.NET or Windows Service application), then you can just delete this method.
#### **XPS Stream and Print Programming Sample**
This code example convert a Diagram into an XPS stream and print.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-XpsPrintHelper-XpsPrint_PrintDocument.cs" >}}


The second XpsPrintHelper.Print overload accepts a Stream object. The stream must contain a document in the XPS format. This method starts an XPS print job, sends the document to the XpsPrint API and then waits for the result if needed.
#### **XpsPrint API Programming Sample**
This code example prints an XPS document using the XpsPrint API.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-XpsPrintHelper-XpsPrint_PrintStream.cs" >}}


The code for the StartJob, CopyJob, WaitForJob and CheckJobStatus methods as well as definitions of the IXpsPrintJob and IXpsPrintJobStream interfaces is quite low-level and uses Platform Invoke and COM Interop. This code is not included in the article for brevity, but it is available in the sample download.

The XpsPrint API also provides additional functionality, such as monitoring the job progress, but our XpsPrintHelper is a very simple wrapper and does not expose this functionality. You could add this yourself if you want to.

{{% alert color="primary" %}}

When you run the project, it prints a sample document on the specified printer. To make results visible, the console window opens. The program displays the success message or the text of an exception if one was thrown.

{{% /alert %}}
## **Printing a Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net) provides four overloads methods for printing of the diagrams. These methods are flexible enough to print the diagram to the default printer or to any of the available printer with customized settings. You only need to select the appropriate print method according to the requirement.
### **Printing to default printer**
Printing of the diagram to the default printer is quite simple in Aspose.Diagram for .NET. Perform the following steps in order to print the diagram to default printer:

- Create an instance of Diagram class to load a diagram that is to be printed
- Call the Print method with no parameters as exposed by the Diagram object
#### **Printing to Default Printer Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-ByDefaultPrinter-ByDefaultPrinter.cs" >}}
### **Printing to specific printer**
Printing of the diagram to the specific printer requires the name of the printer as parameter to the Print method of the Diagram. Perform the following steps in order to print the diagram to the desired printer:

- Create an instance of Diagram class to load a diagram that is to be printed
- Call the Print method of the Diagram class with printer name as string parameter to the Print method
#### **Printing to Specific Printer Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-BySpecificPrinter-BySpecificPrinter.cs" >}}
### **Setting Printer and Document Name**
Aspose.Diagram APIs allows to set the specific printer and document name for a print job. Perform the following steps in order to print the diagram to the desired printer:

- Create an instance of Diagram class to load a diagram that is to be printed
- Call the Print method of the Diagram class with printer and document name as string parameter to the Print method
#### **Setting Printer and Document Name Programming Sample**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPrintJobAndPrinterName-SetPrintJobAndPrinterName.cs" >}}
