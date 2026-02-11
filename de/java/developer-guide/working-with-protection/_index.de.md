---
title: Arbeiten mit Schutz
type: docs
weight: 90
url: /de/java/working-with-protection/
---
## **Stellen Sie den Schutz der Visio Diagram ein**
 Durch das Schützen von Diagrammen können Benutzer Hintergründe, Vorlagen (Schablonen), Formen und Stile sperren, sodass sie nicht bearbeitet werden können. Dies ist beispielsweise nützlich, um Unternehmensstile zu schützen und ein konsistentes Erscheinungsbild über eine Reihe von Diagrammen hinweg sicherzustellen. Entwickler können dies mit erreichen[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Bearbeiten Sie den Schutz der Visio Diagram**
 Die Methoden getProtectBkgnds, getProtectMasters, getProtectShapes und getProtectStyles, die von der bereitgestellt werden[Dokumenteinstellungen](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentSettings) -Klasse unterstützt das Objekt com.aspose.diagram.BoolValue. Diese Eigenschaften können verwendet werden, um Microsoft Visio Diagramme zu schützen und den Schutz aufzuheben.

In Microsoft Visio schützen Sie Dokumente auf diese Weise:

1. Öffnen Sie eine diagram in Microsoft Visio.
1. Öffnen Sie das Zeichnungs-Explorer-Fenster.
1.  Klicken Sie mit der rechten Maustaste auf eine diagram und wählen Sie sie aus**Dokument schützen** aus dem Menü.
1. Aktivieren oder deaktivieren Sie im Fenster Dokument schützen die Optionen zum Sperren oder Entsperren verschiedener diagram-Elemente.
1.  Klicken**OK**.

**Bitte sehen Sie, wie wir Optionen manuell überprüfen oder löschen können.** 

![todo: Bild_alt_Text](working-with-protection_1.png)

Verwenden Sie den folgenden Code in einer Java-Anwendung, um dieselben Aufgaben auszuführen – sperren und entsperren Sie verschiedene Elemente Ihrer diagram – mit Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioDiagramProtection.class);
//Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");

diagram.getDocumentSettings().setProtectBkgnds(BOOL.TRUE);
diagram.getDocumentSettings().setProtectMasters(BOOL.TRUE);
diagram.getDocumentSettings().setProtectShapes(BOOL.TRUE);
diagram.getDocumentSettings().setProtectStyles(BOOL.TRUE);
// save diagram
diagram.save(dataDir + "VisioDiagramProtection_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

### **Bearbeiten Sie den Formschutz Visio**
 Durch das Schützen von Visio-Formen können Benutzer bestimmte Aspekte von Formen sperren. Zu den Aspekten von Formen, die durch Formschutz gesperrt werden können, gehören Breite, Höhe, x-Position, y-Position, Rotation und mehr. Entwickler können dies mit erreichen[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 Das**getLockAspect()**, **getLockBegin()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **getLockDelete()**, **getLockEnd()**, **getLockFormat()**, **getLockFromGroupFormat()**, **getLockGroup()**, **getLockHeight()**, **getLockMoveX()**, **getLockMoveY()**, **getLockRotate()**, **getLockSelect()**, **getLockTextEdit()**, **getLockThemeColors()**, **getLockThemeEffects()**, **getLockVtxEdit()** und**getLockWidth()** Methoden ausgesetzt durch die[Schutz](https://reference.aspose.com/diagram/java/com.aspose.diagram/Protection) -Klasse unterstützt das Objekt com.aspose.diagram.BoolValue. Diese Methoden können verwendet werden, um Formen zu schützen/den Schutz aufzuheben.

In Visio müssen Sie die folgenden Aktionen ausführen, um eine beliebige Form zu schützen:

1. Öffnen Sie eine diagram in Microsoft Visio.
1. Wählen Sie eine Form aus.
1.  Auswählen**Schutz** von dem**Format** Menü (Visio 2007) oder auswählen**Schutz** von dem**Entwickler** Menü (Visio 2010).
1.  In dem**Schutz** Fenster, aktivieren oder deaktivieren Sie Optionen zum Sperren oder Entsperren von Formattributen.
1.  Klicken**OK**.

**Die Schutzoptionen einer Form, wie in Microsoft Visio zu sehen** 

![todo: Bild_alt_Text](working-with-protection_2.png)

Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um mit Aspose.Diagram for Java dasselbe zu tun (beliebiges Formattribut sperren/entsperren).


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioShapeProtection.class);
//Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);

// set protections
shape.getProtection().getLockAspect().setValue(BOOL.TRUE);
shape.getProtection().getLockBegin().setValue(BOOL.TRUE);
shape.getProtection().getLockCalcWH().setValue(BOOL.TRUE);
shape.getProtection().getLockCrop().setValue(BOOL.TRUE);
shape.getProtection().getLockCustProp().setValue(BOOL.TRUE);
shape.getProtection().getLockDelete().setValue(BOOL.TRUE);
shape.getProtection().getLockEnd().setValue(BOOL.TRUE);
shape.getProtection().getLockFormat().setValue(BOOL.TRUE);
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.TRUE);
shape.getProtection().getLockGroup().setValue(BOOL.TRUE);
shape.getProtection().getLockHeight().setValue(BOOL.TRUE);
shape.getProtection().getLockMoveX().setValue(BOOL.TRUE);
shape.getProtection().getLockMoveY().setValue(BOOL.TRUE);
shape.getProtection().getLockRotate().setValue(BOOL.TRUE);
shape.getProtection().getLockSelect().setValue(BOOL.TRUE);
shape.getProtection().getLockTextEdit().setValue(BOOL.TRUE);
shape.getProtection().getLockThemeColors().setValue(BOOL.TRUE);
shape.getProtection().getLockThemeEffects().setValue(BOOL.TRUE);
shape.getProtection().getLockVtxEdit().setValue(BOOL.TRUE);
shape.getProtection().getLockWidth().setValue(BOOL.TRUE);
        
// save diagram
diagram.save(dataDir + "VisioShapeProtection_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

