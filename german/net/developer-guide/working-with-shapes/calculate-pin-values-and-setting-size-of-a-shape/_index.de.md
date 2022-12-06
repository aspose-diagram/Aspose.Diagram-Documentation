---
title: Berechnen Sie Pin-Werte und legen Sie die Größe einer Form fest
type: docs
weight: 60
url: /de/net/calculate-pin-values-and-setting-size-of-a-shape/
description: In diesem Abschnitt wird erläutert, wie PinX- und PinY-Werte der Unterform mit Aspose.Diagram berechnet werden.
---
## **Berechnen Sie PinX- und PinY-Werte der Unterform**
 Wenn die Form ein untergeordneter Knoten einer Gruppenform ist, ist ihre xform eine relative Koordinate ihrer übergeordneten Form, aber keine absolute Koordinate in der[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page). Wenn der Benutzer die absolute Koordinate erhalten möchte, hilft dieser Beispielcode.

Ein in lokalen Koordinaten angegebener Punkt kann in übergeordnete Koordinaten konvertiert werden, indem die folgenden Transformationen in der folgenden Reihenfolge angewendet werden:

1. Subtrahieren Sie den Wert der LocPinX-Eigenschaft des Cell_Type-Elements von der x-Koordinate.
1. Subtrahieren Sie den Wert der LocPinY-Eigenschaft von Cell_Type von der y-Koordinate.
1. Spiegeln Sie den Punkt um die y-Achse, wenn der Wert der FlipX-Eigenschaft von Cell_Type gleich eins ist.
1. Spiegeln Sie den Punkt um die x-Achse, wenn der Wert der FlipY-Eigenschaft von Cell_Type gleich eins ist.
1. Drehen Sie den Punkt gegen den Uhrzeigersinn um den Ursprung um den Wert der Angle-Eigenschaft von Cell_Type.
1. Addieren Sie den Wert von PinX Cell_Type zur x-Koordinate.
1. Addieren Sie den Wert von PinY Cell_Type zur y-Koordinate.
### **Berechnen Sie PinX und PinY Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um PinX- und PinY-Werte einer Unterform mit Aspose.Diagram for .NET API zu berechnen.







{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-CalculateCenterOfSubShapes-CalculateCenterOfSubShapes.cs" >}}
## **Einstellen von Höhe und Breite einer Form**
 Das[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Mit der Klasse können Sie die Größe der Form steuern, indem Sie die Höhe und Breite der Form mit den Methoden SetHeight und SetWidth angeben.

 Die Methoden SetHeight und SetWidth, verfügbar gemacht durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)Klasse, unterstützt die Größenänderung einer Form mit dem Master, ohne den Master oder in Form einer Gruppenform. Die Codebeispiele in diesem Artikel legen Höhe und Breite fest, um die Größe der Form auf der Seite zu ändern.

Der Vorgang zum Einstellen von Höhe und Breite ist:

1. Laden Sie eine diagram.
1. Finden Sie eine bestimmte Form.
1. Legen Sie die Höhe einer Form fest.
1. Legen Sie die Breite einer Form fest.
1. Speichern Sie die diagram.
### **Programmierungsbeispiel für Höhe und Breite einstellen**
Das folgende Code-Snippet zeigt, wie Sie die Höhe und Breite der Form festlegen. Der Code sucht nach einem Shape-Namensrechteck mit der Shape-ID 1 und legt seine Höhe und Breite auf doppelt fest.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ChangeShapeSize-ChangeShapeSize.cs" >}}
