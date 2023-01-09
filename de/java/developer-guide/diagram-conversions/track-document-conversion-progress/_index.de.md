---
title: Verfolgen Sie den Fortschritt der Dokumentenkonvertierung
type: docs
weight: 970
url: /de/java/track-document-conversion-progress/
description: In diesem Abschnitt wird erläutert, wie Sie den Konvertierungsfortschritt von visio-Dateien mit Aspose.Diagram verfolgen.
---
## **Mögliche Nutzungsszenarien**

Manchmal kann das Konvertieren großer visio-Dateien einige Zeit dauern. Während dieser Zeit möchten Sie möglicherweise den Fortschritt der Dokumentkonvertierung statt nur eines Ladebildschirms anzeigen, um die Benutzerfreundlichkeit Ihrer Anwendung zu verbessern. Aspose.Diagram unterstützt die Verfolgung des Dokumentenkonvertierungsprozesses durch Bereitstellen der IPageSavingCallback-Schnittstelle. Die IPageSavingCallback-Schnittstelle stellt die Methoden PageStartSaving und PageEndSaving bereit, die Sie in Ihrer benutzerdefinierten Klasse implementieren können. Sie können auch steuern, welche Seiten gerendert werden, wie im T*estDiagramPageSavingCallback*benutzerdefinierte Klasse.

## **Verfolgen Sie den Fortschritt der Dokumentenkonvertierung**

 Das folgende Codebeispiel lädt die[Quelldatei visio](Drawing1.vsdx) und druckt seinen Konvertierungsfortschritt in der Konsole mithilfe von*TestPageSavingCallback*benutzerdefinierte Klasse, die die IPageSavingCallback-Schnittstelle implementiert.

## **Beispielcode**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}

Das Folgende ist der Code für die*TestDiagramPageSavingCallback*benutzerdefinierte Klasse.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}

## **Konsolenausgabe**

Beginnen Sie mit dem Speichern des Seitenindex 0 der Seiten 11</br>
Beenden Sie das Speichern des Seitenindex 0 der Seiten 11</br>
Beginnen Sie mit dem Speichern von Seitenindex 1 von Seite 11</br>
Beenden Sie das Speichern des Seitenindex 1 der Seite 11</br>
Beginnen Sie mit dem Speichern von Seitenindex 2 von Seite 11</br>
Beenden Sie das Speichern des Seitenindex 2 der Seite 11</br>
Beginnen Sie mit dem Speichern von Seitenindex 3 von Seite 11</br>
Beenden Sie das Speichern des Seitenindex 3 der Seite 11</br>
Beginnen Sie mit dem Speichern von Seitenindex 4 von Seite 11</br>
Beenden Sie das Speichern von Seitenindex 4 von Seite 11</br>
Beginnen Sie mit dem Speichern von Seitenindex 5 von Seite 11</br>
Beenden Sie das Speichern des Seitenindex 5 der Seite 11</br>
Beginnen Sie mit dem Speichern von Seitenindex 6 von Seite 11</br>
Beenden Sie das Speichern des Seitenindex 6 der Seite 11</br>
Beginnen Sie mit dem Speichern von Seitenindex 7 von Seite 11</br>
Beenden Sie das Speichern des Seitenindex 7 von Seite 11</br>
Beginnen Sie mit dem Speichern von Seitenindex 8 der Seiten 11</br>
Beenden Sie das Speichern des Seitenindex 8 der Seite 11
