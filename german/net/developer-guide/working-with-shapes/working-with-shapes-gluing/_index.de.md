---
title: Arbeiten mit Shapes Gluing
type: docs
weight: 40
url: /de/net/working-with-shapes-gluing/
description: In diesem Abschnitt wird erklärt, wie Sie Formen erhalten, die mit Aspose.Diagram an eine bestimmte Form geklebt werden.
---
## **Holen Sie sich die Steckverbinder in eine bestimmte Form geklebt**
[Visio Formen hinzufügen und verbinden](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) erklärt, wie man eine Form hinzufügt und sie mit anderen Formen in Microsoft Visio Diagrammen unter Verwendung von Aspose.Diagram for .NET verbindet. Es ist auch möglich, Verbinder zu finden, die an diese Form geklebt sind.
### **Geklebte Formen erhalten**
 Die GluedShapes-Methode, die von der bereitgestellt wird[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)-Klasse kann verwendet werden, um eine Liste der IDs aller Konnektoren zu erhalten, die an eine Form geklebt sind, oder, wenn die betreffende Form eine Konnektor ist, die IDs der Formen, mit denen sie verbunden ist[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) Klasse, kann dann verwendet werden, um eine Form anhand ihrer ID zu finden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Greifen Sie auf eine bestimmte Form zu.
1. Rufen Sie eine Liste der IDs aller Verbindungsstücke ab, die an dieses Shape geklebt sind.
#### **Holen Sie sich Connectors Glued Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um alle Verbinder zu finden, die mit Aspose.Diagram for .NET an eine Form geklebt wurden.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GetGluedConnectors-GetGluedConnectors.cs" >}}
## **Visio Formen mit Verbindungspunkt zusammenkleben**
Aspose.Diagram for .NET ermöglicht es Entwicklern, Formen durch die Verbindungspunkte zusammenzukleben.
### **Formen kleben**
 Die GlueShapes-Methode, die von der bereitgestellt wird[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Klasse verwendet werden kann.

|<p>**Geben Sie diagram ein** </p><p>![todo: Bild_alt_Text](working-with-shapes-gluing_1.png)</p>|<p>**Die diagram nach dem Kleben der Formen** </p><p>![todo: Bild_alt_Text](working-with-shapes-gluing_2.png)</p>|
|:- |:- |
Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Formen kleben.
1. Speichern Sie diagram.
#### **Glue Visio Formen Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer Anwendung .NET, um Formen durch die Verbindungspunkte zu kleben:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueVisioShapes-GlueVisioShapes.cs" >}}
## **Kleben Sie Formen in den Behälter**
Aspose.Diagram for .NET ermöglicht es Entwicklern, Gruppenformen in einen Container zu kleben.
### **Leimgruppenform**
 Die GlueShapesInContainer-Methode, die von der bereitgestellt wird[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Klasse verwendet werden kann.

|<p>**Geben Sie diagram ein** </p><p>![todo: Bild_alt_Text](working-with-shapes-gluing_3.png)</p>|<p>**Die diagram nach dem Kleben der Gruppenformen** </p><p>![todo: Bild_alt_Text](working-with-shapes-gluing_4.png)</p>|
|:- |:- |
Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Gruppenformen kleben.
1. Speichern Sie diagram.
#### **Glue Shapes Inside Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um die Gruppenform in einen Container zu kleben:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueContainerShape-GlueContainerShape.cs" >}}
