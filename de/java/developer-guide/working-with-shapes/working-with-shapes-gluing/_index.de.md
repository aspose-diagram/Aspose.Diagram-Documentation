---
title: Arbeiten mit Shapes Gluing
type: docs
weight: 10
url: /de/java/working-with-shapes-gluing/
---
## **Holen Sie sich die Steckverbinder in eine bestimmte Form geklebt**
[Visio Formen hinzufügen und verbinden](/diagram/de/java/add-and-connect-visio-shapes/) erklärt, wie man eine Form hinzufügt und sie mit anderen Formen in Microsoft Visio Diagrammen unter Verwendung von Aspose.Diagram for Java verbindet. Es ist auch möglich, Verbinder zu finden, die an diese Form geklebt sind.
### **Geklebte Formen erhalten**
 Die GluedShapes-Methode, die von der bereitgestellt wird[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)-Klasse kann verwendet werden, um eine Liste der IDs aller Konnektoren zu erhalten, die an eine Form geklebt sind, oder, wenn die betreffende Form eine Konnektor ist, die IDs der Formen, mit denen sie verbunden ist[ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) Klasse, kann dann verwendet werden, um eine Form anhand ihrer ID zu finden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Greifen Sie auf eine bestimmte Form zu.
1. Rufen Sie eine Liste der IDs aller Verbindungsstücke ab, die an dieses Shape geklebt sind.
#### **Holen Sie sich Connectors Glued Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um alle Verbinder zu finden, die mit Aspose.Diagram for Java an eine Form geklebt wurden.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GetGluedConnectors-GetGluedConnectors.java" >}}
## **Visio Formen mit Verbindungspunkt zusammenkleben**
Aspose.Diagram for Java ermöglicht es Entwicklern, Formen durch die Verbindungspunkte zusammenzukleben.
### **Formen kleben**
 Die GlueShapes-Methode, die von der bereitgestellt wird[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) Klasse verwendet werden kann.

|<p>**Geben Sie diagram ein** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/Z69f4hg.png)</p>|<p>**Die diagram nach dem Kleben der Formen** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/5TJpDwc.png)</p>|
|:- |:- |
Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Formen kleben.
1. Speichern Sie diagram.
#### **Glue Visio Formen Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer Anwendung Java, um Formen durch die Verbindungspunkte zu kleben:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueVisioShapes-GlueVisioShapes.java" >}}
## **Kleben Sie Formen in den Behälter**
Aspose.Diagram for Java ermöglicht es Entwicklern, Gruppenformen in einen Container zu kleben.
### **Leimgruppenform**
Die GlueShapesInContainer-Methode, die von der Page-Klasse verfügbar gemacht wird, kann verwendet werden.

|<p>**Geben Sie diagram ein** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/HRRzIEh.png)</p>|<p>**Die diagram nach dem Kleben der Gruppenformen** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/YxCiOgU.png)</p>|
|:- |:- |
Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Gruppenformen kleben.
1. Speichern Sie diagram.
#### **Glue Shapes Inside Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um die Gruppenform in einen Container zu kleben:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueContainerShape-GlueContainerShape.java" >}}
