---
title: Drehen, ändern Sie die Position und verbinden Sie Unterformen
type: docs
weight: 30
url: /de/net/rotate-change-the-position-and-connect-sub-shapes/
description: In diesem Abschnitt wird erläutert, wie Sie eine visio-Form mit Aspose.Diagram drehen.
---
## **Drehen Sie eine Form mit einem geeigneten Winkel**
 Mit Aspose.Diagram for .NET können Sie eine Form in einen beliebigen Winkel drehen. Die SetAngle-Methode, die von der bereitgestellt wird[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) -Klasse kann verwendet werden, um eine Form in jeden gewünschten Winkel zu drehen. Es nimmt einen einzelnen Parameter als Winkel an.
### **Drehen eines Formprogrammierungsbeispiels**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um eine Form mit Aspose.Diagram for .NET zu drehen.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RotateVisioShape-RotateVisioShape.cs" >}}
## **Ändern Sie die Position einer Form**
 Das[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Mit der Klasse können Sie die Position einer Form ändern. Die Verbindungslinie passt sich automatisch an, wenn die Form an eine andere Position verschoben wird. Die Move- und MoveTo-Methoden, die von verfügbar gemacht werden[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, unterstützen Sie das Ändern der Position einer Form als Teil einer Gruppe oder nicht. Die Codebeispiele in diesem Artikel verschieben eine Form auf der Seite.

Der Vorgang zum Verschieben einer Form ist:

1. Laden Sie eine diagram.
1. Finden Sie eine bestimmte Form.
1. Verschieben Sie die Form an einen anderen Ort
1. Speichern Sie die diagram.
### **Beispiel für die Programmierung der Position ändern**
Das folgende Code-Snippet zeigt, wie die Form verschoben wird. Der Code ruft eine Visio-Seite nach Name und Form nach ID 16 ab und verschiebt ihre Position.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-MoveVisioShape-MoveVisioShape.cs" >}}
## **Verbinden Sie Unterformen der Gruppen**
 In diesem Thema wird erläutert, wie zwei Unterformen von zwei verschiedenen Gruppenformen in Microsoft Visio-Diagrammen mithilfe von Aspose.Diagram for .NET verbunden werden. Die ConnectShapesViaConnector-Methode, die von der[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page) Klasse kann verwendet werden, um die Shapes über ihre IDs zu verbinden. Die AddShape-Methode, verfügbar gemacht durch die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)Klasse, kann verwendet werden, um eine Form hinzuzufügen.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Greifen Sie auf eine bestimmte Seite zu.
1. Fügen Sie der ausgewählten Seite eine dynamische Verbindungsform hinzu.
1. Unterformen verbinden
### **Programmierbeispiel für Teilformen verbinden**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um die Unterformen von zwei verschiedenen Gruppenformen mit Aspose.Diagram for .NET zu verbinden.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ConnectVisioSubShapes-ConnectVisioSubShapes.cs" >}}
## **Holen Sie sich die Formen, die mit einer bestimmten Form verbunden sind**
[Visio Formen hinzufügen und verbinden](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) erklärt, wie man eine Form hinzufügt und sie mit anderen Formen in Microsoft Visio Diagrammen unter Verwendung von Aspose.Diagram for .NET verbindet. Es ist auch möglich, Formen zu finden, die mit einer bestimmten Form verbunden sind.

 Die ConnectedShapes-Methode, die von der bereitgestellt wird[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) -Klasse kann verwendet werden, um die IDs der Shapes zu erhalten, die mit einem Shape verbunden sind. Die GetShape-Methode, verfügbar gemacht durch die[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) Klasse, kann dann verwendet werden, um eine Form anhand ihrer ID zu finden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. Greifen Sie auf eine bestimmte Form zu.
1. Rufen Sie die Namen aller Formen ab, die mit der ausgewählten Form verbunden sind.
### **Holen Sie sich Shapes-Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um alle Formen zu finden, die mit einer bestimmten Form verbunden sind, die Aspose.Diagram for .NET verwendet.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GetAllConnectedShapes-GetAllConnectedShapes.cs" >}}
