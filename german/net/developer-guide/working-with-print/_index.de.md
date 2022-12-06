---
title: Arbeiten mit Drucken
type: docs
weight: 80
url: /de/net/working-with-print/
description: In diesem Abschnitt wird erläutert, wie Sie ein Dokument über XpsPrint mit Aspose.Diagram drucken.
---
## **So drucken Sie ein Dokument auf einem Server über XpsPrint API**
Dieser Artikel kann für alle nützlich sein, die ein XPS-Dokument aus einer .NET-Anwendung an das nicht verwaltete XpsPrint API senden möchten. Das Hauptziel dieses Artikels besteht jedoch darin, zu zeigen, wie ein diagram aus einer ASP.NET- oder Windows-Dienstanwendung mit Aspose.Diagram und XpsPrint API gedruckt wird.
### **Problem**
Wenn Sie eine .NET-Anwendung entwickeln und Druckausgaben erstellen müssen, können Sie die Klassen im System.Drawing.Printing-Namespace oder die WPF-Klassen verwenden. Wenn Sie jedoch eine ASP.NET- oder Windows-Dienstanwendung entwickeln, sind Ihre Möglichkeiten zum Drucken stark eingeschränkt, da Microsoft davon abrät, diese Ansätze zu verwenden. Weitere Informationen finden Sie unter den folgenden Links.

<http://support.microsoft.com/kb/324565>

Die Verwendung der .NET Framework Druckklassen wird nicht von einem Dienst unterstützt. Dazu gehören ASP-Seiten, die in der Regel im Kontext des Serverdienstes laufen.

<http://msdn.microsoft.com/en-us/library/system.drawing.printing.aspx>

Klassen innerhalb des System.Drawing.Printing-Namespace werden nicht für die Verwendung in einem Windows-Dienst oder einer ASP.NET-Anwendung oder einem Dienst unterstützt. Der Versuch, diese Klassen innerhalb eines dieser Anwendungstypen zu verwenden, kann zu unerwarteten Problemen führen, wie z. B. einer verringerten Dienstleistung und Laufzeitausnahmen.

<http://msdn.microsoft.com/en-us/library/bb613549.aspx>

Die Verwendung von WPF zum Erstellen von Windows-Diensten wird nicht unterstützt. Da es sich bei WPF um eine Präsentationstechnologie handelt, erfordert der Dienst Windows die entsprechenden Berechtigungen, um visuelle Vorgänge auszuführen, die eine Benutzerinteraktion beinhalten. Wenn der Dienst Windows nicht über die entsprechenden Berechtigungen verfügt, kann es zu unerwarteten Ergebnissen kommen.

Das Document-Objekt stellt eine Familie von Print-Methoden zum Drucken von Dokumenten bereit, und diese Methoden drucken über die .NET-Druckklassen, die im System.Drawing.Printing-Namespace definiert sind. Es gibt viele Kunden von Aspose.Diagram, die diese Druckmethode problemlos in ihren serverseitigen Anwendungen verwenden, aber es gibt eine Möglichkeit, den Empfehlungen von Microsoft zu entsprechen, und sie wird in diesem Artikel beschrieben.
### **Lösung**
Der richtige Weg zum Drucken von Dokumenten gemäß Microsoft ist die Verwendung des nicht verwalteten XpsPrint API. Dieser API ist auf Windows 7, Windows Server 2008 R2 und auch auf Windows Vista verfügbar, vorausgesetzt, das Plattform-Update für Windows Vista ist installiert.

Da Aspose.Diagram problemlos jedes Dokument in XPS konvertieren kann, müssen wir nur Code schreiben, der ein XPS-Dokument an XpsPrint API übergibt. Das einzige Problem besteht darin, dass XpsPrint API nicht verwaltet wird und einige Kenntnisse des Plattformaufrufs erfordert.
### **Der Code**
Wir haben die XpsPrintHelper-Klasse mit der Print-Methode erstellt, die sehr einfach zu verwenden ist. Sie müssen lediglich ein zu druckendes Dokument, einen Druckernamen und einen optionalen Auftragsnamen angeben. Wenn beim Senden oder Drucken des Dokuments ein Problem aufgetreten ist, löst die Methode eine Ausnahme aus.

Der letzte Parameter ist ein boolescher Wert, der angibt, ob der Code warten soll, bis der Auftrag gedruckt ist, oder sofort zurückkehren soll, nachdem der Druckauftrag gesendet wurde. Wenn Sie sich für eine sofortige Rückkehr entscheiden, können Sie am Ende nicht feststellen, ob das Dokument erfolgreich gedruckt wurde oder nicht.
#### **Programmierbeispiel**
Das folgende Codebeispiel zeigt, wie die Hilfsklasse zum Drucken über XPS aufgerufen wird.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-PrintDiagramVisXPSPrinterAPI-PrintDiagramVisXPSPrinterAPI.cs" >}}


Es gibt zwei Überladungen der XpsPrintHelper.Print-Methode. Die erste Überladung nimmt ein Aspose.Diagram.Diagram-Objekt und speichert es in einem MemoryStream im XPS-Format. Dann wird die andere XpsPrintHelper.Print-Überladung aufgerufen.

Wenn Sie dieses Beispiel ohne Aspose.Diagram verwenden möchten (z. B. wenn Sie bereits ein XPS-Dokument haben und es nur aus einer ASP.NET- oder Windows-Dienstanwendung drucken möchten), können Sie diese Methode einfach löschen.
#### **Programmierbeispiel für XPS Stream und Print**
Dieses Codebeispiel konvertiert eine Diagram in einen XPS-Stream und druckt.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-XpsPrintHelper-XpsPrint_PrintDocument.cs" >}}


Die zweite XpsPrintHelper.Print-Überladung akzeptiert ein Stream-Objekt. Der Stream muss ein Dokument im XPS-Format enthalten. Diese Methode startet einen XPS-Druckauftrag, sendet das Dokument an den XpsPrint API und wartet dann ggf. auf das Ergebnis.
#### **XpsPrint API Programmierbeispiel**
Dieses Codebeispiel druckt ein XPS-Dokument mit dem XpsPrint API.

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
