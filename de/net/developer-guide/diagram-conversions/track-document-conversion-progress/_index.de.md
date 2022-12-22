---
title: Verfolgen Sie den Fortschritt der Dokumentenkonvertierung
type: docs
weight: 970
url: /de/net/track-document-conversion-progress/
description: In diesem Abschnitt wird erläutert, wie Sie den Konvertierungsfortschritt von visio-Dateien mit Aspose.Diagram verfolgen.
---
## **Mögliche Nutzungsszenarien**

 Manchmal kann das Konvertieren großer visio-Dateien einige Zeit dauern. Während dieser Zeit möchten Sie möglicherweise den Fortschritt der Dokumentkonvertierung statt nur eines Ladebildschirms anzeigen, um die Benutzerfreundlichkeit Ihrer Anwendung zu verbessern. Aspose.Diagram unterstützt die Verfolgung des Dokumentenkonvertierungsprozesses durch Bereitstellung der**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)** Schnittstelle. Das**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**Schnittstelle bietet**[PageStartSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pagestartsaving)**und**[PageEndSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pageendsaving)**Methoden, die Sie in Ihrer benutzerdefinierten Klasse implementieren können. Sie können auch steuern, welche Seiten gerendert werden, wie im T*estDiagramPageSavingCallback*benutzerdefinierte Klasse.

## **Verfolgen Sie den Fortschritt der Dokumentenkonvertierung**

 Das folgende Codebeispiel lädt die[Quelldatei visio](Drawing1.vsdx) und druckt seinen Konvertierungsfortschritt in der Konsole mithilfe von*TestPageSavingCallback* benutzerdefinierte Klasse, die die implementiert**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**Schnittstelle.

## **Beispielcode**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-DocumentConversionProgress-1.cs" >}}

Das Folgende ist der Code für die*TestDiagramPageSavingCallback*benutzerdefinierte Klasse.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-DocumentConversionProgress-2.cs" >}}

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
