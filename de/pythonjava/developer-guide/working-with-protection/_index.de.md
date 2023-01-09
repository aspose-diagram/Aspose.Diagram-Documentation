---
title: Arbeiten mit Schutz
type: docs
weight: 90
url: /de/python-java/working-with-protection/
---
## **Stellen Sie den Schutz der Visio Diagram ein**
Protecting diagrams allow users to lock backgrounds, masters (stencils), shapes and styles so that they cannot be edited. This is useful for protecting corporate styles, for example, and ensure a consistent look across a set of diagrams. Developers can achieve this using Aspose.Diagram for Python via Java.

### **Bearbeiten Sie den Schutz der Visio Diagram**
Die Methoden getProtectBkgnds, getProtectMasters, getProtectShapes und getProtectStyles, die von der DocumentSettings-Klasse bereitgestellt werden, unterstützen das BoolValue-Objekt. Diese Eigenschaften können verwendet werden, um Microsoft Visio Diagramme zu schützen und den Schutz aufzuheben.

In Microsoft Visio schützen Sie Dokumente auf diese Weise:

1. Öffnen Sie eine diagram in Microsoft Visio.
1. Öffnen Sie das Zeichnungs-Explorer-Fenster.
1.  Klicken Sie mit der rechten Maustaste auf eine diagram und wählen Sie sie aus**Dokument schützen** aus dem Menü.
1. Aktivieren oder deaktivieren Sie im Fenster Dokument schützen die Optionen zum Sperren oder Entsperren verschiedener diagram-Elemente.
1.  Klicken**OK**.

**Bitte sehen Sie, wie wir Optionen manuell überprüfen oder löschen können.** 

Use the code below in your application to perform the same tasks – lock and unlock different elements of your diagram – using Aspose.Diagram for Python via Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioDiagramProtection.py" >}}

### **Bearbeiten Sie den Formschutz Visio**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using Aspose.Diagram for Python via Java.

 Das**getLockAspect()**, **getLockBegin()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **getLockDelete()**, **getLockEnd()**, **getLockFormat()**, **getLockFromGroupFormat()**, **getLockGroup()**, **getLockHeight()**, **getLockMoveX()**, **getLockMoveY()**, **getLockRotate()**, **getLockSelect()**, **getLockTextEdit()**, **getLockThemeColors()**, **getLockThemeEffects()**, **getLockVtxEdit()** und**getLockWidth()** Methoden ausgesetzt durch die**Schutz** -Klasse unterstützt das BoolValue-Objekt. Diese Methoden können verwendet werden, um Formen zu schützen/den Schutz aufzuheben.

In Visio müssen Sie die folgenden Aktionen ausführen, um eine beliebige Form zu schützen:

1. Öffnen Sie eine diagram in Microsoft Visio.
1. Wählen Sie eine Form aus.
1.  Auswählen**Schutz** von dem**Format** Menü (Visio 2007) oder auswählen**Schutz** von dem**Entwickler** Menü (Visio 2010).
1.  In dem**Schutz** Fenster, aktivieren oder deaktivieren Sie Optionen zum Sperren oder Entsperren von Formattributen.
1.  Klicken**OK**.

**Die Schutzoptionen einer Form, wie in Microsoft Visio zu sehen** 

Use the following code in your Java application to do the same thing (lock/unlock any shape attribute) using Aspose.Diagram for Python via Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioShapeProtection.py" >}}
