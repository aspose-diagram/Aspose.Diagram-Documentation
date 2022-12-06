---
title: Verwendung von Aspose.Diagram in anderen Programmiersprachen
type: docs
weight: 120
url: /de/net/utilizing-aspose-diagram-in-other-programming-languages/
description: Diese Seite beschreibt, wie Sie Aspose.Diagram in anderen Programmiersprachen verwenden.
---
## **Verwenden Sie Aspose.Diagram for .NET über COM Interop**
 Die Informationen in diesem Thema gelten für Szenarien, in denen Entwickler verwenden müssen[Aspose.Diagram for .NET](/diagram/de/net/home/) über COM Interop in jeder unterstützten Sprache.
### **Arbeiten mit COM-Interop**
Aspose.Diagram for .NET wird unter der Kontrolle von .NET Framework ausgeführt und dies wird verwalteter Code genannt. Der in all diesen Sprachen geschriebene Code läuft außerhalb der .NET Framework und wird als nicht verwalteter Code bezeichnet. Die Interaktion zwischen nicht verwaltetem Code und Aspose.Diagram erfolgt über die .NET-Einrichtung namens COM Interop.

Aspose.Diagram-Objekte sind .NET-Objekte, aber wenn sie über COM Interop verwendet werden, erscheinen sie als COM-Objekte in Ihrer Programmiersprache. Stellen Sie daher am besten sicher, dass Sie wissen, wie COM-Objekte in Ihrer Programmiersprache erstellt und verwendet werden, bevor Sie mit der Verwendung beginnen[Aspose.Diagram for .NET](/diagram/de/net/home/).

- In der COM-Welt unterscheiden wir COM-Server und COM-Client. Der COM-Server speichert COM-Klassen, während der COM-Client den COM-Server nach Klasseninstanzen, dh COM-Objekten, fragt.
-  Der COM-Client oder einfach die Client-Anwendung kann etwas über den Inhalt der COM-Klasse wissen oder sich seiner Methoden und Eigenschaften überhaupt nicht bewusst sein. Daher kann die Clientanwendung die COM-Klassenstruktur beim Kompilieren/Erstellen oder nur während der Ausführung erkennen. Der Prozess der "Entdeckung" ist als Bindung bekannt, und das haben wir auch**frühe Bindung** und**späte Bindung**.
- Kurz gesagt, die COM-Klasse ist wie eine Blackbox, und um mit ihr zu arbeiten, wird eine Typbibliothek benötigt. Diese Binärdatei enthält eine Beschreibung der COM-Klassenmethoden, Eigenschaften und jede Hochsprache, die das Arbeiten mit COM-Objekten unterstützt. Oft hat sie einen Syntaxausdruck zum Hinzufügen einer Typbibliothek, z Beispiel ist dies[**#importieren**](http://msdn.microsoft.com/en-us/library/8etzzkb6.aspx) unter C++.
- Typbibliothek wird für die frühe Bindung verwendet.
-  Ein COM-Objekt kann seine Methoden und Eigenschaften auf zwei Arten offenlegen: durch a**Versandschnittstelle** (dispatchinterface) und in seiner**vtable** (virtuelle Funktionstabelle).
-  innerhalb der**Verteilerschnittstelle** , wird jede Methode und Eigenschaft durch ein eindeutiges Mitglied identifiziert; Dieses Mitglied ist die Dispatch-ID der Funktion (oder**DispID**).
- **vtable** ist nur ein Satz von Zeigern auf Funktionen, die die COM-Klassenschnittstelle unterstützt.
-  Ein Objekt, das seine Methoden über beide Schnittstellen offenlegt, unterstützt a**duale Schnittstelle**.
- Beide Bindungsarten haben Vorteile. Die frühe Bindung bietet Ihnen eine verbesserte Leistung und Syntaxprüfung zur Kompilierzeit. Spätes Binden ist am vorteilhaftesten, wenn Sie Kunden schreiben, die Sie beabsichtigen zu sein***kompatibel mit zukünftigen Versionen*** Ihrer COM-Klasse. Bei der späten Bindung werden Informationen aus der Typbibliothek nicht in Ihrem Client "fest verdrahtet", sodass Sie sich darauf verlassen können, dass Ihr Client mit zukünftigen Versionen der COM-Klasse ohne Codeänderungen arbeiten kann.
-  Der späte Bindungsmechanismus hat einen großen Vorteil: Wenn der Ersteller der COM-DLL beschließt, eine neue Version mit einem anderen Layout der Funktionsschnittstelle herauszugeben, stürzt jeglicher Code, der diese Methoden aufruft, nicht ab, es sei denn, die Methoden sind nicht mehr verfügbar; auch wenn die**vtable**unterscheidet sich die späte Bindung, um die neuen DISPIDs zu entdecken und geeignete Methoden aufzurufen.

 Hier sind die Themen, die Sie schließlich meistern müssen:

- Verwenden von COM-Objekten in Ihrer Programmiersprache. Siehe die Dokumentation zu Ihrer Programmiersprache und die sprachspezifischen Themen weiter unten in dieser Dokumentation.
-  Arbeiten mit COM-Objekten, die von .NET COM Interop verfügbar gemacht werden. Sehen[Interoperieren mit nicht verwaltetem Code](https://docs.microsoft.com/en-us/dotnet/framework/interop/) und[.NET Framework Komponenten COM aussetzen](https://docs.microsoft.com/en-us/dotnet/framework/interop/exposing-dotnet-components-to-com) im MSDN.
-  Aspose.Diagram Dokumentobjektmodell. Sehen[Aspose.Diagram Programmierhandbuch](https://docs.aspose.com/diagram/net/developer-guide/) und[API Referenz](https://reference.aspose.com/diagram/net).
#### **Registrieren Sie Aspose.Diagram for .NET bei COM Interop**
Sie müssen Aspose.Diagram for .NET installieren und sicherstellen, dass es bei COM Interop registriert ist (um sicherzustellen, dass es von nicht verwaltetem Code aufgerufen werden kann).

So registrieren Sie Aspose.Diagram for .NET manuell für COM Interop:

1.  Von dem**Anfang** Menü, auswählen**Alle Programme** , dann**Microsoft Visual Studio**, **Visual Studio-Tools** und schlussendlich,**Visual Studio-Eingabeaufforderung**. In einigen Betriebssystemen ist es auch unter folgendem Speicherort verfügbar: „C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\bin\x64“
1.  Geben Sie den Befehl ein, um die Assembly zu registrieren:
   1. .NET Framework 2.0
regasm "C:\Programme\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /codebase
   1. .NET Framework 3.5
 regasm "C:\Programme\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /codebase
   1. .NET Framework 4.0
 regasm "C:\Programme\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /codebase

{{% alert color="primary" %}} 

Beachten Sie, dass /codebase nur erforderlich ist, wenn sich Aspose.Diagram.dll nicht im GAC befindet. Wenn Sie diese Option verwenden, wird regasm den Pfad für die Assemblierung in die Registrierung einfügen.

{{% /alert %}} {{% alert color="primary" %}} 

 regasm.exe ist ein Tool, das im .NET Framework SDK enthalten ist. Alle .NET Framework SDK-Tools befinden sich in der*\Microsoft .NET\Framevork\<FrameworkVersion>* Verzeichnis zum Beispiel*C:\Windows\Microsoft .NET\Framework\v4.0.30319*. Wenn Sie Visual Studio .NET verwenden:
 Von dem**Anfang** Menü, auswählen**Programme** , gefolgt von**Microsoft Visual Studio .NET** , dann**Visual Studio .NET-Tools** und schlussendlich,**Visual Studio .NET 2003 Eingabeaufforderung**.
Es führt eine Eingabeaufforderung mit allen erforderlichen Umgebungsvariablen aus.

{{% /alert %}} 
##### **ProgIDs**
ProgID steht für „Programmatic Identifier“. Es ist der Name einer COM-Klasse, die zum Erstellen eines Objekts verwendet wurde. ProgIDs bestehen aus dem Bibliotheksnamen „Aspose.Diagram“ und dem Klassennamen.
##### **Geben Sie Bibliothek ein**
Wenn Ihre Programmiersprache (z. B. Visual Basic oder Delphi) den Verweis auf eine COM-Typbibliothek zulässt, fügen Sie einen Verweis auf Aspose.Diagram.tlb hinzu, um alle Aspose.Diagram for .NET Klassen, Methoden, Eigenschaften und Aufzählungen in Ihrem Objektbrowser anzuzeigen.

So generieren Sie eine TLB-Datei:

- .NET Framework 2.0
 regasm "C:\Programme\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /tlb: "C:\Programme\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.tlb" /codebase
- .NET Framework 3.5
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.tlb" /codebase
- .NET Framework 4.0
regasm "C:\Programme\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /tlb: "C:\Programme\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.tlb" /codebase
#### **Erstellen von COM-Objekten**
Die Erstellung eines COM-Objekts ähnelt der Erstellung eines normalen .NET-Objekts. Nach der Erstellung können Sie auf die Methoden und Eigenschaften des Objekts zugreifen, als wäre es ein COM-Objekt.

Einige Methoden haben Überladungen und werden von COM-Interop mit einem hinzugefügten numerischen Suffix verfügbar gemacht, mit Ausnahme der allerersten Methode, die unverändert bleibt. Beispielsweise werden die Methodenüberladungen Diagram.Save zu Diagram.Save, Diagram.Save_2 usw.

{{% alert color="primary" %}} 

 Weitere Informationen finden Sie in den sprachspezifischen Artikeln weiter unten in dieser Dokumentation.

{{% /alert %}} 
## **Aspose.Diagram Ressourcen**
Im Folgenden finden Sie Links zu einigen nützlichen Ressourcen, die Sie möglicherweise zur Erfüllung Ihrer Aufgaben benötigen.
- [Aspose.Diagram for Java Online-Dokumentation](https://docs.aspose.com/diagram/java/)
- [Aspose.Diagram für Node.js über Java Online-Dokumentation](https://docs.aspose.com/diagram/nodejsjava/)
- [Aspose.Diagram für Python über Java Online-Dokumentation](https://docs.aspose.com/diagram/pythonjava/)

##### **Erstellen einer Wrapper-Assembly**
Wenn Sie viele der Aspose.Diagram for .NET Klassen, Methoden und Eigenschaften verwenden müssen, sollten Sie eine Wrapper-Assembly erstellen (mit C# oder einer anderen .NET Programmiersprache). Wrapper-Assemblys tragen dazu bei, die Verwendung von Aspose.Diagram for .NET direkt aus nicht verwaltetem Code zu vermeiden.

Ein guter Ansatz besteht darin, eine .NET-Assembly zu entwickeln, die auf Aspose.Diagram for .NET verweist und die gesamte Arbeit damit erledigt und nur einen minimalen Satz von Klassen und Methoden für nicht verwalteten Code verfügbar macht. Ihre Anwendung sollte dann nur mit Ihrer Wrapper-Bibliothek funktionieren.

 Das Reduzieren der Anzahl der Klassen und Methoden, die Sie über COM-Interop aufrufen müssen, vereinfacht das Projekt. Die Verwendung von .NET-Klassen über COM Interop erfordert häufig fortgeschrittene Kenntnisse.
## **Erstellen Sie eine leere Visio-Zeichnung in PHP mit COM Interop**
### **Voraussetzungen**
 Konfigurieren Sie Ihr PHP so, dass es mit COM funktioniert. Sehen<http://www.php.net/manual/en/ref.com.php> . Weitere Informationen finden Sie im genannten Artikel[Verwenden Sie Aspose.Diagram for .NET über COM Interop](/diagram/de/net/home/).
### **Erstellen einer leeren Visio-Zeichnung**
 Dies ist eine einfache Anwendung, die Ihnen zeigt, wie Sie eine leere Visio-Zeichnung mit erstellen[Aspose.Diagram for .NET](/diagram/de/net/home/) in PHP über COM-Interop.

**PHP**

{{< highlight "csharp" >}}

 <?php

echo "<h3>Calling Aspose.Diagram for .NET from PHP using COM Interoperatibility</h3>";

//set license

$lic = new COM("Aspose.Diagram.License");

$lic->SetLicense("D:\ASPOSE\Licences\Aspose.Total licenses\Aspose.Total.lic");

// create a new instance of Diagram object using COM interop

$diagram = new COM("Aspose.Diagram.Diagram");

// Save the Visio drawing in the VDX format

$diagram->Save("d:\diagramtest\MyOutput.vdx", 0);

?>



{{< /highlight >}}
