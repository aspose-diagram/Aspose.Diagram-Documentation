---
title: Erhalten Sie Warninformationen beim Speichern der Datei Visio
type: docs
weight: 110
url: /de/net/get-warning-information-while-saving-visio-file/
---
## **Mögliche Nutzungsszenarien**

 Manchmal versucht der Benutzer, die diagram zu speichern, die Text enthält, der keine lokale Schriftart hat. In diesem Fall gibt Aspose.Diagram beim Speichern von diagram Warnungen aus. Sie können diese Warnungen abfangen, indem Sie die implementieren**[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)** Schnittstelle und Einstellung**[SaveOptions.WarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)**Eigentum.

## **Erhalten Sie Warnungen beim Speichern der Visio-Datei**

 Der folgende Beispielcode erläutert, wie Sie beim Speichern der Datei visio Warnungen erhalten. Der Code konvertiert die[Beispieldatei visio](sampleFontSubstitution.vsdx) der wirft**[FontSubstitution] (https://reference.aspose.com/diagram/net/aspose.diagram/warningtype)** Warnung beim Speichern. Diese Warnung wird dann abgefangen**[IWarningCallback.Warning()](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)**Methode, die die Warnmeldungen auf der Konsole ausgibt. Bitte überprüfen Sie zum besseren Verständnis auch die Konsolenausgabe des unten angegebenen Codes.

## **Beispielcode**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-GetWarningInformation.cs" >}}

## **Konsolenausgabe**

Hier ist die Konsolenausgabe des obigen Codes, wenn er mit dem bereitgestellten ausgeführt wird[Beispieldatei visio](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
