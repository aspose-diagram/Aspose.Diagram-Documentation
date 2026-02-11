---
title: Lizenzierung
type: docs
weight: 50
url: /de/net/licensing/
description: Aspose. Diagram for .NET lädt seine Kunden ein, eine Classic-Lizenz und eine Metered-Lizenz zu erwerben. Verwenden Sie außerdem eine eingeschränkte Lizenz, um das Produkt besser zu erkunden.
---
## **Aspose.Diagram auswerten**
Sie können das Produkt Aspose.Diagram for .NET einfach zu Testzwecken herunterladen. Bitte wende dich an die[Aspose.Diagram for .NET Download-Seite](https://www.nuget.org/packages/Aspose.Diagram/)um die neuste Version herauszufinden. Der Evaluierungs-Download ist derselbe wie der gekaufte Download. Die Evaluierungsversion wird einfach lizenziert, wenn Sie einige Codezeilen hinzufügen, um die Lizenz anzuwenden.

Die Evaluierungsversion von Aspose.Diagram (ohne Angabe einer Lizenz) bietet die volle Produktfunktionalität, fügt jedoch beim Öffnen und Speichern ein Evaluierungswasserzeichen in die Mitte des Dokuments ein und beschränkt das Lesen nur der ersten zehn Formen der ersten Seite Ihres Visio diagram .

![todo: Bild_alt_Text](licensing_1.png)
### **Einschränkungen der Evaluierungsversion**
Die Evaluierungsversion bietet alle Funktionen mit Ausnahme der folgenden:

- Sie können nur die ersten zehn Formen der ersten Seite von Visio diagram lesen.
- You will also see evaluation watermark in exported images and PDF files.

{{% alert color="primary" %}} 

 Wenn Sie Aspose.Diagram ohne Evaluierungseinschränkungen ausprobieren möchten, fordern Sie eine temporäre 30-Tage-Lizenz an. Bitte beziehen Sie sich auf[Wie erhalte ich eine temporäre Lizenz?](https://purchase.aspose.com/temporary-license) für mehr Informationen.

{{% /alert %}} 
## **Anwenden einer Lizenz**
Sobald Sie mit Ihrem zufrieden sind[Auswertung](https://downloads.aspose.com/diagram/net) von Aspose.Diagram for .NET, kaufen Sie eine Lizenz auf der Aspose-Website:[Einkaufsportal](https://purchase.aspose.com/buy) . Machen Sie sich mit den verschiedenen verfügbaren Lizenztypen vertraut. Wenn Sie irgendwelche Fragen haben,[Wenden Sie sich an das Verkaufsteam unter Aspose](https://about.aspose.com/contact) und sie helfen Ihnen gerne weiter.

Jede Aspose-Lizenz enthält ein einjähriges Abonnement für kostenlose Upgrades auf alle neuen Versionen oder Fixes, die während dieser Zeit herauskommen. Wir bieten sowohl lizenzierten als auch Evaluierungsbenutzern kostenlosen und unbegrenzten technischen Support.

Die Lizenz ist eine reine Text-XML-Datei, die Details wie den Produktnamen, die Anzahl der lizenzierten Entwickler, das Ablaufdatum des Abonnements usw. enthält. Die Datei ist digital signiert, ändern Sie die Datei also nicht: Selbst das Hinzufügen eines zusätzlichen Zeilenumbruchs zur Datei macht sie ungültig.
### **Wann eine Lizenz beantragt werden sollte**
Befolgen Sie diese einfachen Regeln:

- Die Lizenz muss nur einmal pro Anwendungsdomäne festgelegt werden.
- Sie müssen die Lizenz festlegen, bevor Sie andere Aspose.Diagram-Klassen verwenden.
- Das mehrmalige Aufrufen von SetLicense schadet nicht, verschwendet aber Prozessorzeit.
- Wenn Sie eine Windows Forms- oder Konsolenanwendung entwickeln, rufen Sie SetLicense im Startcode auf, bevor Sie Aspose.Diagram-Klassen verwenden.
- Rufen Sie beim Entwickeln einer ASP.NET-Anwendung SetLicense aus der Datei Global.asax.cs in der geschützten Methode Aplication_Start auf. Es wird einmal aufgerufen, wenn die Anwendung gestartet wird.
- Rufen Sie SetLicense nicht innerhalb der Page_Load-Methoden auf, da dies bedeutet, dass die Lizenz jedes Mal geladen wird, wenn eine Webseite geladen wird.
- Wenn Sie eine Klassenbibliothek entwickeln, rufen Sie SetLicense von einem statischen Konstruktor der Klasse auf, die Aspose.Diagram verwendet. Der statische Konstruktor wird ausgeführt, bevor eine Instanz Ihrer Klasse erstellt wird, und stellt sicher, dass die Aspose.Diagram-Lizenz richtig festgelegt ist.
### **Wenden Sie die Lizenz mit dem Datei- oder Stream-Objekt an**
 Verwenden Sie die[Lizenz.SetLicense](https://reference.aspose.com/diagram/net/aspose.diagram/license)Methode zum Lizenzieren der Komponente. Der einfachste Weg, eine Lizenz festzulegen, besteht darin, die Lizenzdatei in denselben Ordner wie die Aspose.Diagram.dll zu legen und den Dateinamen ohne Pfad anzugeben, wie unten gezeigt.
#### **Laden einer Lizenz aus einer Datei**
Dieses Code-Snippet initialisiert eine Lizenz, die in einer Datei oder in einer eingebetteten Ressource gespeichert ist.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// Set path of the license file, i.e. c:\temp\
string dataDir = @"c:\temp\";

License license = new License();
license.SetLicense(dataDir + "Aspose.Diagram.lic");

{{< /highlight >}}
```
#### **Laden einer Lizenz aus einem Stream-Objekt**
Diese Codeausschnitte initialisieren die Lizenz aus dem Stream.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// Set path of the license file, i.e. c:\temp\
string dataDir = @"c:\temp\";
// Load an existing Visio file in the stream
FileStream LicStream = new FileStream(dataDir + "Aspose.Diagram.lic", FileMode.Open);

License license = new License();
license.SetLicense(LicStream);

{{< /highlight >}}
```
## **Wenden Sie eine gemessene Lizenz an**
Aspose.Diagram for .NET API ermöglicht es Entwicklern, eine gemessene Lizenz anzuwenden. Es ist ein neuer Lizenzierungsmechanismus. Der neue Lizenzierungsmechanismus wird zusammen mit der bestehenden Lizenzierungsmethode verwendet. Diejenigen Kunden, die basierend auf der Nutzung der API-Funktionen abgerechnet werden möchten, können die gebührenpflichtige Lizenzierung verwenden. Weitere Einzelheiten finden Sie unter[Häufig gestellte Fragen zur getakteten Lizenzierung](https://purchase.aspose.com/faqs/licensing/metered)Sektion.

Eine neue Klasse[Gemessen](https://reference.aspose.com/diagram/net/aspose.diagram/metered)wurde hinzugefügt, um einen gemessenen Schlüssel anzuwenden. Dieses Codebeispiel zeigt, wie gemessene öffentliche und private Schlüssel festgelegt werden:

```
{{< highlight "csharp" >}}
// Initialize a Metered license class object
Aspose.Diagram.Metered metered = new Aspose.Diagram.Metered();
// apply public and private keys
metered.SetMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}
```
