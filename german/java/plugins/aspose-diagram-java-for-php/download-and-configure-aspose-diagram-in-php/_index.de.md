---
title: Laden Sie Aspose.Diagram in PHP herunter und konfigurieren Sie es
type: docs
weight: 10
url: /de/java/download-and-configure-aspose-diagram-in-php/
---
## **Erforderliche Bibliotheken herunterladen**
Laden Sie die unten aufgeführten erforderlichen Bibliotheken herunter. Diese sind für die Ausführung von Aspose.Diagram Java für Ruby-Beispiele erforderlich.

- [Aspose.Diagram for Java Komponente](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram)
## **Laden Sie Beispiele von Social-Coding-Sites herunter**
Die folgenden Versionen von Laufbeispielen stehen auf den unten genannten Social-Coding-Sites zum Download zur Verfügung:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/tree/master/Plugins/Aspose_Diagram_Java_for_PHP)
## **Installieren**
Es ist sehr einfach und leicht, Aspose.Diagram Java für PHP zu installieren, bitte folgen Sie den Anweisungen:

Führen Sie folgenden Befehl aus.

{{< highlight "java" >}}

 $ gem install asposediagramjava

{{< /highlight >}}
## **Verwenden**
Schließen Sie die erforderlichen Dateien ein, um die Zeichnung visio in ein PDF-Dokument zu exportieren.

{{< highlight "java" >}}

 require File.dirname(File.dirname(File.dirname(__FILE__))) + '/lib/asposediagramjava'

include Asposediagramjava

include Asposediagramjava::ExportToPdf

initialize_aspose_Diagram

{{< /highlight >}}

Lassen Sie uns den obigen Code verstehen.

1. Die erste Zeile stellt sicher, dass die Aspose.Diagram geladen und verfügbar ist.
1. Schließen Sie die Dateien ein, die für den Zugriff auf die Aspose.Diagram erforderlich sind
1. Initialisieren Sie die Bibliotheken. Die Klassen aspose Java werden aus dem Pfad geladen, der in der Datei aspose.yml angegeben ist
