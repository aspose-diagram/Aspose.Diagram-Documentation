---
title: Konfigurieren von Schriftarten für das Rendern
type: docs
weight: 10
url: /de/net/configuring-fonts-for-rendering/
---
## **Mögliche Nutzungsszenarien**

Aspose.Diagram APIs bieten die Möglichkeit, Seiten in Bildformaten zu rendern und sie in PDF- und XPS-Formate zu konvertieren. Um die Konvertierungstreue zu maximieren, müssen die in der Tabelle verwendeten Schriftarten im Standardverzeichnis für Schriftarten des Betriebssystems verfügbar sein. Falls die erforderlichen Schriftarten nicht vorhanden sind, versuchen die Aspose.Diagram-APIs, die erforderlichen Schriftarten durch die verfügbaren zu ersetzen.

## **Auswahl an Schriftarten**

Unten ist der Prozess, dem Aspose.Diagram-APIs hinter den Kulissen folgen.

1. Der API versucht, die Schriftarten im Dateisystem zu finden, die genau mit dem in der Tabelle verwendeten Schriftartnamen übereinstimmen.
1.  Wenn API die unter definierte Schriftart nicht finden kann**[SaveOptions.DefaultFont](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/defaultfont/)** -Eigenschaft versucht es, die unter angegebene Schriftart zu verwenden**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)**Eigentum.
1.  Wenn API die unter definierte Schriftart nicht finden kann**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)** -Eigenschaft versucht es, die am besten geeigneten Schriftarten aus allen verfügbaren Schriftarten auszuwählen.
1. Wenn schließlich API keine Schriftarten im Dateisystem finden kann, wird die Seite mit Times New Roman gerendert.

## **Legen Sie benutzerdefinierte Schriftordner fest**

 Aspose.Diagram APIs durchsuchen das Standardverzeichnis für Schriftarten des Betriebssystems nach den erforderlichen Schriftarten. Falls die erforderlichen Schriftarten nicht im Schriftartenverzeichnis des Systems verfügbar sind, durchsuchen die APIs die benutzerdefinierten (benutzerdefinierten) Verzeichnisse. Das**[FontConfigs](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/)** Die Klasse hat eine Reihe von Möglichkeiten zum Festlegen benutzerdefinierter Schriftartenverzeichnisse gezeigt, wie unten beschrieben.

1. **[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)**: Diese Methode ist nützlich, wenn nur ein Ordner festgelegt werden soll.

1. **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)**Diese Methode ist nützlich, wenn sich die Schriftarten in mehreren Ordnern befinden und der Benutzer alle Ordner separat festlegen möchte, anstatt alle Schriftarten in einem einzigen Ordner zu kombinieren.
1. **[FontConfigs.SetFontSources](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontsources/)**Hinweis: Dieser Mechanismus ist nützlich, wenn der Benutzer Schriftarten aus mehreren Ordnern oder eine einzelne Schriftartdatei oder Schriftartdaten aus einem Array von Bytes laden möchte.

{{% alert color="primary" %}}

 Beide**[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)** & **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)** Methoden akzeptieren einen zweiten Parameter vom Typ Boolean. Vorbeigehen**Stimmt** da der zweite Parameter die Aspose.Diagram-APIs anweist, die Unterordner nach den Schriftartdateien zu durchsuchen.

{{% /alert %}}

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-OS-Fonts-Location-SetCustomFontFolders-SetCustomFontFolders.cs" >}}

{{% alert color="primary" %}}

Bitte verwenden Sie zu Beginn der Bewerbung eine der oben genannten Methoden, d.h. bevor andere Objekte von Aspose.Diagram-APIs aufgerufen werden.

{{% /alert %}} {{% alert color="primary" %}}

Wenn alle oben genannten Methoden zum Einstellen der Schriftartquellen verwendet werden, werden nur die letzten Einstellungen wirksam.

{{% /alert %}}

