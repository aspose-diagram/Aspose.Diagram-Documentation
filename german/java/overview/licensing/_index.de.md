---
title: Lizenzierung
type: docs
weight: 60
url: /de/java/licensing/
---
## **Einschränkungen der Evaluierungsversion**
 Eine kostenlose Testversion von Aspose.Diagram for Java kann heruntergeladen werden[Aspose Aufbewahrungsort](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram).
### **Einschränkung**
Die Evaluierungsversion bietet alle Funktionen mit Ausnahme der folgenden:

- Sie können nur die ersten zehn Formen der ersten Seite Ihrer VSD-Datei lesen.
- You will also see evaluation watermark in exoprted images and PDF files.

 Wenn Sie Aspose.Diagram ohne Evaluierungseinschränkungen ausprobieren möchten, fordern Sie eine temporäre 30-Tage-Lizenz an. Bitte beziehen Sie sich auf[Wie erhalte ich eine temporäre Lizenz?](https://purchase.aspose.com/temporary-license) für mehr Informationen.
## **Anwenden einer Lizenz**
 Sie können eine Evaluierungsversion von herunterladen**Aspose.Diagram** for Java ab[Aspose Aufbewahrungsort](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram). Die Evaluierungsversion bietet absolut dieselben Funktionen wie die lizenzierte Version des Produkts. Darüber hinaus wird die Evaluierungsversion einfach lizenziert, wenn Sie eine Lizenz erwerben und ein paar Codezeilen hinzufügen, um die Lizenz anzuwenden.

 Sobald Sie mit Ihrer Bewertung zufrieden sind**Aspose.Diagram** , du kannst[eine Lizenz erwerben](https://purchase.aspose.com/buy) auf der Website Aspose. Machen Sie sich mit den verschiedenen angebotenen Abonnementarten vertraut. Bei Fragen steht Ihnen das Verkaufsteam unter Aspose gerne zur Verfügung.

Jede Aspose-Lizenz enthält ein einjähriges Abonnement für kostenlose Upgrades auf alle neuen Versionen oder Fixes, die während dieser Zeit herauskommen. Der technische Support ist kostenlos und unbegrenzt und wird sowohl lizenzierten als auch Testbenutzern zur Verfügung gestellt.

{{% alert color="primary" %}} 

 Wenn Sie testen möchten**Aspose.Diagram** ohne Einschränkungen der Testversion, fordern Sie eine temporäre 30-Tage-Lizenz an. Bitte beziehen Sie sich auf[Wie erhalte ich eine temporäre Lizenz?](https://purchase.aspose.com/temporary-license) für mehr Informationen.

{{% /alert %}} 
### **Einstellen einer Lizenz**
Die Lizenz ist eine reine Text-XML-Datei, die Details wie den Produktnamen, die Anzahl der lizenzierten Entwickler, das Ablaufdatum des Abonnements usw. enthält. Die Datei ist digital signiert, ändern Sie die Datei also nicht; selbst das versehentliche Hinzufügen eines zusätzlichen Zeilenumbruchs in der Datei macht sie ungültig.

Sie müssen eine Lizenz anwenden, bevor Sie Vorgänge mit Dokumenten durchführen. Stellen Sie sicher, dass Sie dies tun, bevor Sie ein Diagram-Objekt erstellen. Sie müssen nur einmal pro Anwendung oder Prozess eine Lizenz festlegen.

Die Lizenz kann aus einem Stream oder einer Datei an den folgenden Orten geladen werden:

1. Explizite Pfad.
1. Der Ordner, der die Datei Aspose.Diagram.jar enthält.

 Verwenden Sie die[Lizenz.setLicense()](https://reference.aspose.com/diagram/java/com.aspose.diagram/License) Methode zum Lizenzieren der Komponente. Der einfachste Weg, eine Lizenz festzulegen, besteht oft darin, die Lizenzdatei in denselben Ordner wie Aspose.Diagram.jar zu legen und nur den Dateinamen ohne Pfad anzugeben, wie im folgenden Beispiel gezeigt:
#### **Beispiel 1**
 In diesem Beispiel**Aspose.Diagram** versucht, die Lizenzdatei in dem Ordner zu finden, der die JARs Ihrer Anwendung enthält.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense("Aspose.Diagram.Java.lic");

{{< /highlight >}}
#### **Beispiel 2**
Initialisiert eine Lizenz aus einem Stream.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense(new java.io.FileInputStream("Aspose.Diagram.Java.lic"));

{{< /highlight >}}
### **Validieren Sie die Lizenz**
 Es ist möglich, zu überprüfen, ob die Lizenz richtig eingestellt wurde oder nicht. Das[Lizenz](https://reference.aspose.com/diagram/java/com.aspose.diagram/License)Die Klasse hat das isLicensed-Feld, das „true“ zurückgibt, wenn die Lizenz richtig eingestellt wurde.

**Java**

{{< highlight "csharp" >}}

 License license = new License();

license.setLicense("Aspose.Diagram.Java.lic");

if (License.isLicensed()) {

    System.out.println("License is Set!");

}

{{< /highlight >}}
## **Wenden Sie eine gemessene Lizenz an**
Aspose.Diagram for Java API ermöglicht es Entwicklern, eine gemessene Lizenz anzuwenden. Es ist ein neuer Lizenzierungsmechanismus. Der neue Lizenzierungsmechanismus wird zusammen mit der bestehenden Lizenzierungsmethode verwendet. Diejenigen Kunden, die basierend auf der Nutzung der API-Funktionen abgerechnet werden möchten, können die gebührenpflichtige Lizenzierung verwenden. Weitere Einzelheiten finden Sie unter[Häufig gestellte Fragen zur getakteten Lizenzierung](https://purchase.aspose.com/faqs/licensing/metered)Sektion.

Eine neue Klasse[Gemessen](https://reference.aspose.com/diagram/java/com.aspose.diagram/Metered) wurde hinzugefügt, um einen gemessenen Schlüssel anzuwenden. Dieses Codebeispiel zeigt, wie gemessene öffentliche und private Schlüssel festgelegt werden:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-License-PublicAndPrivateKeys-PublicAndPrivateKeys.java" >}}
