---
title: Konfigurieren Sie Visio TimeLine-Shapes
type: docs
weight: 20
url: /de/java/configure-visio-timeline-shapes/
---
## **Legen Sie die Eigenschaften der Meilensteinform fest**
Aspose.Diagram ermöglicht es Entwicklern, Meilensteineigenschaften festzulegen. Dieser Artikel zeigt, wie Sie das Datum des Meilensteins, das Datumsformat, das Flag und den Typ für die automatische Aktualisierung festlegen.
### **Festlegen von Meilensteindatum, Datumsformat, Auto-Update-Flag und Typ**
 Das[MeilensteinHelfer](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)Klasse dauert ein[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Objekt beim Initialisieren der[MeilensteinHelfer](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper) Objekt. Das Codebeispiel in diesem Artikel legt die Eigenschaften Meilensteindatum, Datumsformat, Kennzeichen für automatische Aktualisierung und Meilensteintyp fest.

|<p>**Der Meilenstein vor dem Update** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/XulWyBC.png)</p><p>\</p>|<p>**Der Meilenstein nach dem Update. Beachten Sie das geänderte Datumsformat.** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/cMJQNch.png)</p><p>\</p>|
|:- |:- |
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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-SetMilestoneProps-SetMilestoneProps.java" >}}


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
 Das[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper)Klasse dauert ein[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) Objekt beim Initialisieren der[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) Objekt. Das Codebeispiel in diesem Artikel legt die Start-, End- und Datumsformatwerte für den Zeitraum fest.

|<p>**Die Registerkarte „Zeitraum“ des Dialogfelds „Visio Zeitleiste konfigurieren“.** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/nHth3W8.png)</p>|<p>**Die Registerkarte „Zeitformat“ des Dialogfelds „Visio Zeitleiste konfigurieren“.** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/TxFKc1K.png)</p>|
|:- |:- |
|<p>**Geben Sie diagram ein** </p><p>![todo: Bild_alt_Text](configure-visio-timeline-shapes_1.png)</p>|<p>**Die diagram nachdem die Werte geändert wurden** </p><p>![todo: Bild_alt_Text](configure-visio-timeline-shapes_2.png)</p>|
Der Prozess zum Aktualisieren des Start-, End- und Datumsformats des Zeitraums ist:

1. Laden Sie eine diagram.
1. Finden Sie eine bestimmte Form.
1. Initialisieren Sie das TimeLineHelper-Objekt.
1. Legen Sie den Beginn des Zeitraums fest.
1. Stellen Sie das Ende des Zeitraums ein.
1. Legen Sie ein Datumsformat fest.
1. Speichern Sie die Zeichnung Visio in einem beliebigen unterstützten Format.
#### **Programmierungsbeispiel für Zeitraum und Datum einstellen**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-ConfigureTimeLine-ConfigureTimeLine.java" >}}


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
 Die RefreshTimeLine-Methode, die von der bereitgestellt wird[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) Klasse kann verwendet werden, um Meilensteine auf der Zeitachse wiederzubeleben.

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
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um Meilensteine auf der Zeitachse mit Aspose.Diagram for Java wiederzubeleben.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-RefreshTimeLine-RefreshTimeLine.java" >}}
### **Aktualisieren Sie Meilensteine auf der Timeline mithilfe der MilestoneHelper-Klasse**
 Die RefreshMilestone-Methode, die von der bereitgestellt wird[MeilensteinHelfer](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)-Klasse kann verwendet werden, um Meilensteine auf der Zeitachse zu aktualisieren.

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
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um Meilensteine auf der Zeitachse mit Aspose.Diagram for Java zu aktualisieren.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-RefreshMilestoneWithMilestoneHelper-RefreshMilestoneWithMilestoneHelper.java" >}}
