﻿---
title: Arbeiten mit Drucken
type: docs
weight: 80
url: /de/net/working-with-print/
description: This section explains how to print a document via XpsPrint with Aspose.Diagram.
---
## **How to Print a Document on a Server via the XpsPrint API**
This article can be useful to anyone who wants to submit an XPS document to the unmanaged XpsPrint API from a .NET application. But the main goal if this article is to show how to print a diagram from an ASP.NET or Windows Service application using Aspose.Diagram and the XpsPrint API.
### **Problem**
Wenn Sie eine .NET-Anwendung entwickeln und Druckausgaben erstellen müssen, können Sie die Klassen im System.Drawing.Printing-Namespace oder die WPF-Klassen verwenden. Wenn Sie jedoch eine ASP.NET- oder Windows-Dienstanwendung entwickeln, sind Ihre Möglichkeiten zum Drucken stark eingeschränkt, da Microsoft davon abrät, diese Ansätze zu verwenden. Weitere Informationen finden Sie unter den folgenden Links.

<http://support.microsoft.com/kb/324565>

Die Verwendung der .NET Framework Druckklassen wird nicht von einem Dienst unterstützt. Dazu gehören ASP-Seiten, die in der Regel im Kontext des Serverdienstes laufen.

<http://msdn.microsoft.com/en-us/library/system.drawing.printing.aspx>

Klassen innerhalb des System.Drawing.Printing-Namespace werden nicht für die Verwendung in einem Windows-Dienst oder einer ASP.NET-Anwendung oder einem Dienst unterstützt. Der Versuch, diese Klassen innerhalb eines dieser Anwendungstypen zu verwenden, kann zu unerwarteten Problemen führen, wie z. B. einer verringerten Dienstleistung und Laufzeitausnahmen.

<http://msdn.microsoft.com/en-us/library/bb613549.aspx>

Die Verwendung von WPF zum Erstellen von Windows-Diensten wird nicht unterstützt. Da es sich bei WPF um eine Präsentationstechnologie handelt, erfordert der Dienst Windows die entsprechenden Berechtigungen, um visuelle Vorgänge auszuführen, die eine Benutzerinteraktion beinhalten. Wenn der Dienst Windows nicht über die entsprechenden Berechtigungen verfügt, kann es zu unerwarteten Ergebnissen kommen.

The Document object provides a family of the Print methods to print documents and these methods print via the .NET printing classes defined in the System.Drawing.Printing namespace. There are many customers of Aspose.Diagram who use this printing method in their server-side applications without any problems, but there is a way to comply with Microsoft’s recommendations and it is described in this article.
### **Lösung**
Der richtige Weg zum Drucken von Dokumenten gemäß Microsoft ist die Verwendung des nicht verwalteten XpsPrint API. Dieser API ist auf Windows 7, Windows Server 2008 R2 und auch auf Windows Vista verfügbar, vorausgesetzt, das Plattform-Update für Windows Vista ist installiert.

Since Aspose.Diagram can easily convert any document to XPS, we only need to write code that passes an XPS document to the XpsPrint API. The only problem is that the XpsPrint API is unmanaged and it requires some knowledge of the Platform Invoke.
### **Der Code**
Wir haben die XpsPrintHelper-Klasse mit der Print-Methode erstellt, die sehr einfach zu verwenden ist. Sie müssen lediglich ein zu druckendes Dokument, einen Druckernamen und einen optionalen Auftragsnamen angeben. Wenn beim Senden oder Drucken des Dokuments ein Problem aufgetreten ist, löst die Methode eine Ausnahme aus.

Der letzte Parameter ist ein boolescher Wert, der angibt, ob der Code warten soll, bis der Auftrag gedruckt ist, oder sofort zurückkehren soll, nachdem der Druckauftrag gesendet wurde. Wenn Sie sich für eine sofortige Rückkehr entscheiden, können Sie am Ende nicht feststellen, ob das Dokument erfolgreich gedruckt wurde oder nicht.
#### **Programmierbeispiel**
The following code example shows how to invoke the utility class to print via XPS.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-PrintDiagramVisXPSPrinterAPI-PrintDiagramVisXPSPrinterAPI.cs" >}}


There are two overloads of the XpsPrintHelper.Print method. The first overload takes an Aspose.Diagram.Diagram object and saves it into a MemoryStream in the XPS format. Then it invokes the other XpsPrintHelper.Print overload.

If you want to use this sample without Aspose.Diagram (e.g. you already have an XPS document and just want to print it from an ASP.NET or Windows Service application), then you can just delete this method.
#### **XPS Stream and Print Programming Sample**
This code example convert a Diagram into an XPS stream and print.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-XpsPrintHelper-XpsPrint_PrintDocument.cs" >}}


The second XpsPrintHelper.Print overload accepts a Stream object. The stream must contain a document in the XPS format. This method starts an XPS print job, sends the document to the XpsPrint API and then waits for the result if needed.
#### **XpsPrint API Programmierbeispiel**
This code example prints an XPS document using the XpsPrint API.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-XpsPrintHelper-XpsPrint_PrintStream.cs" >}}


Der Code für die StartJob-, CopyJob-, WaitForJob- und CheckJobStatus-Methoden sowie die Definitionen der IXpsPrintJob- und IXpsPrintJobStream-Schnittstellen ist ziemlich niedrig und verwendet Platform Invoke und COM Interop. Dieser Code ist der Kürze halber nicht im Artikel enthalten, steht aber im Beispieldownload zur Verfügung.

Der XpsPrint API bietet auch zusätzliche Funktionen, wie z. B. die Überwachung des Auftragsfortschritts, aber unser XpsPrintHelper ist ein sehr einfacher Wrapper und stellt diese Funktionalität nicht zur Verfügung. Sie können dies selbst hinzufügen, wenn Sie möchten.

{{% alert color="primary" %}}

Wenn Sie das Projekt ausführen, druckt es ein Beispieldokument auf dem angegebenen Drucker. Um Ergebnisse sichtbar zu machen, öffnet sich das Konsolenfenster. Das Programm zeigt die Erfolgsmeldung oder den Text einer Ausnahme an, falls eine ausgelöst wurde.

{{% /alert %}}
## **Drucken einer Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) bietet vier Überladungsmethoden zum Drucken der Diagramme. Diese Methoden sind flexibel genug, um die diagram auf dem Standarddrucker oder auf einem der verfügbaren Drucker mit benutzerdefinierten Einstellungen zu drucken. Sie müssen lediglich je nach Anforderung das passende Druckverfahren auswählen.
### **Drucken auf Standarddrucker**
Das Drucken von diagram auf dem Standarddrucker ist ganz einfach in Aspose.Diagram for .NET. Führen Sie die folgenden Schritte aus, um diagram auf dem Standarddrucker zu drucken:

- Erstellen Sie eine Instanz der Klasse Diagram, um eine diagram zu laden, die gedruckt werden soll
- Rufen Sie die Print-Methode ohne Parameter auf, wie sie vom Diagram-Objekt verfügbar gemacht wird
#### **Drucken auf Standarddrucker Programmierbeispiel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-ByDefaultPrinter-ByDefaultPrinter.cs" >}}
### **Drucken auf einem bestimmten Drucker**
Das Drucken von diagram auf dem spezifischen Drucker erfordert den Namen des Druckers als Parameter für die Print-Methode von Diagram. Führen Sie die folgenden Schritte aus, um diagram auf dem gewünschten Drucker zu drucken:

- Erstellen Sie eine Instanz der Klasse Diagram, um eine diagram zu laden, die gedruckt werden soll
- Rufen Sie die Print-Methode der Klasse Diagram mit dem Druckernamen als Zeichenfolgenparameter für die Print-Methode auf
#### **Drucken auf einem bestimmten Drucker Programmierbeispiel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-BySpecificPrinter-BySpecificPrinter.cs" >}}
### **Einstellen von Drucker und Dokumentname**
Aspose.Diagram APIs ermöglicht das Festlegen des spezifischen Drucker- und Dokumentnamens für einen Druckauftrag. Führen Sie die folgenden Schritte aus, um die diagram auf dem gewünschten Drucker auszudrucken:

- Erstellen Sie eine Instanz der Klasse Diagram, um eine diagram zu laden, die gedruckt werden soll
- Rufen Sie die Print-Methode der Klasse Diagram mit dem Drucker- und Dokumentnamen als Zeichenfolgenparameter für die Print-Methode auf
#### **Beispiel für die Programmierung des Druckers und des Dokumentnamens**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPrintJobAndPrinterName-SetPrintJobAndPrinterName.cs" >}}
