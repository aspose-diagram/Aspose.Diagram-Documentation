---
title: Konfigurieren Sie Visio TimeLine-Shapes
type: docs
weight: 50
url: /de/net/configure-visio-timeline-shapes/
description: In diesem Abschnitt wird erläutert, wie Sie die Eigenschaft einer Meilensteinform mit Aspose.Diagram festlegen.
---
## **Legen Sie die Eigenschaften der Meilensteinform fest**
Aspose.Diagram ermöglicht es Entwicklern, Meilensteineigenschaften festzulegen. Dieser Artikel zeigt, wie Sie das Datum des Meilensteins, das Datumsformat, das Flag und den Typ für die automatische Aktualisierung festlegen.
### **Festlegen von Meilensteindatum, Datumsformat, Auto-Update-Flag und Typ**
 Das[MeilensteinHelfer](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)Klasse dauert ein[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Objekt beim Initialisieren der[MeilensteinHelfer](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) Objekt. Das Codebeispiel in diesem Artikel legt die Eigenschaften Meilensteindatum, Datumsformat, Kennzeichen für automatische Aktualisierung und Meilensteintyp fest.

Der Vorgang zum Aktualisieren des Meilensteindatums, des Datumsformats, der Markierung für die automatische Aktualisierung und des Meilensteintyps:

1. Laden Sie eine diagram.
1. Finden Sie eine bestimmte Form.
1. Initialisieren Sie das MilestoneHelper-Objekt.
1. Legen Sie ein Meilensteindatum fest.
1. Legen Sie das Meilenstein-Datumsformat fest.
1. Setzen Sie ein Auto-Update-Flag.
1. Legen Sie den Meilensteintyp fest
1. Speichern Sie die Zeichnung Visio in einem beliebigen unterstützten Format.
#### **Programmierbeispiel für Meilenstein setzen**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ConfigureTimeLineShapes-SetMilestoneProps-SetMilestoneProps.cs" >}}


Tabelle der Datumsformatwerte:

|**Wert**|**Zeichenkette formatieren**|
|:- |:- |
|0|dddd, yyyy-Md|
|1|JJJJ-MM-TT|
|2|jj-MMM-d|
|3|JJJJ/M/T|
|4|jj-MMM.-d|
|5|d MMMM jjjj|
|6|jj-M|
|7|MMM-yy|
|8|MMMM d, jjjj|
|9|MMM d, jjjj|
|10|Md-jj|
|11|Md|
|12|d MMMM, jjjj|
|13|d MMM, jjjj|
|14|dM-jj|
|15|dm|
|16|jj-Md|
|17|jjjj-Md|
|18|M-jj|
|19|M-jjjj|
|20|MMMM yyyy|
|21|MMMM ja|
|22|MMM yyyy|
|23|MMM ja|
|24|jj|
|25|jjjj|
|26|d|
|27|MMMM|
|28|MMM|
|29|M|
## **Legen Sie den Zeitraum und das Datumsformat der Zeitachsenform fest**
Aspose.Diagram ermöglicht es Entwicklern, die Zeitleiste programmgesteuert zu konfigurieren. Hier wird erklärt, wie Sie den Zeitraum und das Datumsformat von Zeitachsenformen (Block, Linie, Lineal, geteilt oder zylindrisch) anpassen.
### **Zeitraum und Datumsformat einstellen**
 Das[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper)Klasse dauert ein[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Objekt beim Initialisieren der[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) Objekt. Das Codebeispiel in diesem Artikel legt die Start-, End- und Datumsformatwerte für den Zeitraum fest.

Der Prozess zum Aktualisieren des Start-, End- und Datumsformats des Zeitraums ist:

1. Laden Sie eine diagram.
1. Finden Sie eine bestimmte Form.
1. Initialisieren Sie das TimeLineHelper-Objekt.
1. Legen Sie den Beginn des Zeitraums fest.
1. Stellen Sie das Ende des Zeitraums ein.
1. Legen Sie ein Datumsformat fest.
1. Speichern Sie die Zeichnung Visio in einem beliebigen unterstützten Format.
#### **Programmierungsbeispiel für Zeitraum und Datum einstellen**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ConfigureTimeLineShapes-ConfigureTimeLine-ConfigureTimeLine.cs" >}}


Tabelle der Datumsformatwerte:

|**Wert**|**Zeichenkette formatieren**|
|:- |:- |
|0|dddd, yyyy-Md|
|1|JJJJ-MM-TT|
|2|jj-MMM-d|
|3|JJJJ/M/T|
|4|jj-MMM.-d|
|5|d MMMM jjjj|
|6|jj-M|
|7|MMM-yy|
|8|MMMM d, jjjj|
|9|MMM d, jjjj|
|10|Md-jj|
|11|Md|
|12|d MMMM, jjjj|
|13|d MMM, jjjj|
|14|dM-jj|
|15|dm|
|16|jj-Md|
|17|jjjj-Md|
|18|M-jj|
|19|M-jjjj|
|20|MMMM yyyy|
|21|MMMM ja|
|22|MMM yyyy|
|23|MMM ja|
|24|jj|
|25|jjjj|
|26|d|
|27|MMMM|
|28|MMM|
|29|M|
## **Aktualisieren Sie Meilensteine auf der Zeitachse in Visio**
Aspose.Diagram ermöglicht es Entwicklern, Meilensteine auf den Zeitachsenformen (Block, Linie, Lineal, geteilt oder zylindrisch) entsprechend der Änderung des Zeitraums anzupassen.
### **Aktualisieren Sie Meilensteine auf der Timeline mithilfe der TimeLineHelper-Klasse**
 Die RefreshTimeLine-Methode, die von der bereitgestellt wird[TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) Klasse kann verwendet werden, um Meilensteine auf der Zeitachse wiederzubeleben.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. Holen Sie sich eine Zeitleistenform.
1. Initialisieren Sie das TimeLineHelper-Objekt.
1. Legen Sie den Beginn des Zeitraums fest.
1. stellen Sie das Ende des Zeitraums ein.
1. Datumsformat festlegen (optional).
1. Rufen Sie die RefreshTimeLine-Methode des TimeLineHelper-Objekts auf.
1. außer diagram
#### **Aktualisieren Sie Meilensteine mit dem TimeLineHelper-Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um Meilensteine auf der Zeitachse mit Aspose.Diagram for .NET wiederzubeleben.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ConfigureTimeLineShapes-RefreshTimeLine-RefreshTimeLine.cs" >}}
### **Aktualisieren Sie Meilensteine auf der Timeline mithilfe der MilestoneHelper-Klasse**
 Die RefreshMilestone-Methode, die von der bereitgestellt wird[MeilensteinHelfer](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper)-Klasse kann verwendet werden, um Meilensteine auf der Zeitachse zu aktualisieren.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. Holen Sie sich eine Zeitleistenform.
1. Fügen Sie Shape in Visio diagram mit der AddShape-Methode hinzu.
1. Initialisieren Sie das MilestoneHelper-Objekt.
1. Meilensteindatum festlegen.
1. Setzen Sie die IsAutoUpdate-Eigenschaft von Milstone auf true.
1. Rufen Sie die RefreshMilestone-Methode des MilestoneHelper-Objekts auf.
1. außer diagram
#### **Aktualisieren Sie Meilensteine mit dem MilestoneHelper-Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um Meilensteine auf der Zeitachse mit Aspose.Diagram for .NET zu aktualisieren.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ConfigureTimeLineShapes-RefreshMilestoneWithMilestoneHelper-RefreshMilestoneWithMilestoneHelper.cs" >}}
