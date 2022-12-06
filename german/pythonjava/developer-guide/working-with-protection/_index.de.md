---
title: Arbeiten mit Schutz
type: docs
weight: 90
url: /de/python-java/working-with-protection/
---
## **Stellen Sie den Schutz der Visio Diagram ein**
Durch das Schützen von Diagrammen können Benutzer Hintergründe, Vorlagen (Schablonen), Formen und Stile sperren, sodass sie nicht bearbeitet werden können. Dies ist beispielsweise nützlich, um Unternehmensstile zu schützen und ein konsistentes Erscheinungsbild über eine Reihe von Diagrammen hinweg sicherzustellen. Entwickler können dies erreichen, indem sie Aspose.Diagram für Python über Java verwenden.

### **Bearbeiten Sie den Schutz der Visio Diagram**
Die Methoden getProtectBkgnds, getProtectMasters, getProtectShapes und getProtectStyles, die von der DocumentSettings-Klasse bereitgestellt werden, unterstützen das BoolValue-Objekt. Diese Eigenschaften können verwendet werden, um Microsoft Visio Diagramme zu schützen und den Schutz aufzuheben.

In Microsoft Visio schützen Sie Dokumente auf diese Weise:

1. Öffnen Sie eine diagram in Microsoft Visio.
1. Öffnen Sie das Zeichnungs-Explorer-Fenster.
1.  Klicken Sie mit der rechten Maustaste auf eine diagram und wählen Sie sie aus**Dokument schützen** aus dem Menü.
1. Aktivieren oder deaktivieren Sie im Fenster Dokument schützen die Optionen zum Sperren oder Entsperren verschiedener diagram-Elemente.
1.  Klicken**OK**.

**Bitte sehen Sie, wie wir Optionen manuell überprüfen oder löschen können.** 

Verwenden Sie den folgenden Code in Ihrer Anwendung, um dieselben Aufgaben auszuführen – verschiedene Elemente Ihrer diagram zu sperren und zu entsperren – indem Sie Aspose.Diagram für Python über Java verwenden.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioDiagramProtection.py" >}}

### **Bearbeiten Sie den Formschutz Visio**
Durch das Schützen von Visio-Formen können Benutzer bestimmte Aspekte von Formen sperren. Zu den Aspekten von Formen, die durch Formschutz gesperrt werden können, gehören Breite, Höhe, x-Position, y-Position, Rotation und mehr. Entwickler können dies erreichen, indem sie Aspose.Diagram für Python über Java verwenden.

 Das**getLockAspect()**, **getLockBegin()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **getLockDelete()**, **getLockEnd()**, **getLockFormat()**, **getLockFromGroupFormat()**, **getLockGroup()**, **getLockHeight()**, **getLockMoveX()**, **getLockMoveY()**, **getLockRotate()**, **getLockSelect()**, **getLockTextEdit()**, **getLockThemeColors()**, **getLockThemeEffects()**, **getLockVtxEdit()** und**getLockWidth()** Methoden ausgesetzt durch die**Schutz** -Klasse unterstützt das BoolValue-Objekt. Diese Methoden können verwendet werden, um Formen zu schützen/den Schutz aufzuheben.

In Visio müssen Sie die folgenden Aktionen ausführen, um eine beliebige Form zu schützen:

1. Öffnen Sie eine diagram in Microsoft Visio.
1. Wählen Sie eine Form aus.
1.  Auswählen**Schutz** von dem**Format** Menü (Visio 2007) oder auswählen**Schutz** von dem**Entwickler** Menü (Visio 2010).
1.  In dem**Schutz** Fenster, aktivieren oder deaktivieren Sie Optionen zum Sperren oder Entsperren von Formattributen.
1.  Klicken**OK**.

**Die Schutzoptionen einer Form, wie in Microsoft Visio zu sehen** 

Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um dasselbe zu tun (beliebiges Formattribut zu sperren/entsperren), indem Sie Aspose.Diagram für Python über Java verwenden.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioShapeProtection.py" >}}
