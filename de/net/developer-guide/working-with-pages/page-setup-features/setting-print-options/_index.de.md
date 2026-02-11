---
title: Druckoptionen einstellen
type: docs
weight: 10
url: /de/net/setting-print-options/
description: In diesem Abschnitt wird erläutert, wie Sie Druckoptionen mit Aspose.Diagram festlegen.
---
{{% alert color="primary" %}}

Manchmal ist es erforderlich, Seiteneinrichtungseinstellungen für Seiten zu konfigurieren, um den Druck zu steuern. Diese Seiteneinrichtungseinstellungen bieten verschiedene Optionen.

{{% /alert %}}

## **Druckoptionen einstellen**

Seiteneinrichtungsoptionen werden in Aspose.Diagram vollständig unterstützt. Dieser Artikel erläutert, wie Seitenoptionen mit Aspose.Diagram festgelegt werden, und zeigt Codebeispiele für die Einstellung:

 Aspose.Diagram bietet eine Klasse,[**Buchseite**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , die eine Microsoft Visio-Datei darstellt. Das[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) Klasse enthält a[**Seiten**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) Sammlung, die den Zugriff auf jede Seite in der Datei Visio ermöglicht. Eine Seite wird durch die dargestellt[**Buchseite**](https://reference.aspose.com/diagram/net/aspose.diagram/page)Klasse.

 Das[**Seitenblatt**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) Klasse bietet die[**PrintRequisiten**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) -Eigenschaft, die zum Festlegen der Seiteneinrichtungsoptionen der Seite verwendet wird. In der Tat dies[**PrintRequisiten**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) Eigentum ist ein Objekt der[**Seitenblatt**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) Klasse zum Festlegen verschiedener Seitenlayoutoptionen für eine gedruckte Seite. Das[**PrintRequisiten**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)-Klasse stellt verschiedene Eigenschaften bereit, die zum Festlegen von Seiteneinrichtungsoptionen verwendet werden. Einige dieser Eigenschaften werden unten diskutiert.

### **Ausrichtung der Druckseite**

 Die Druckseitenausrichtung kann mithilfe von auf Hoch- oder Querformat eingestellt werden[**PrintRequisiten**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) Klasse'[**PrintPageOrientation**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) Eigentum. Das[**PrintPageOrientation**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) Die Eigenschaft akzeptiert einen der vordefinierten Werte in der[**PrintPageOrientationValue**](https://reference.aspose.com/diagram/net/aspose.diagram/printpageorientationvalue)Aufzählung, unten aufgeführt.

|**Ausrichtungstypen für Druckseiten**|**Beschreibung**|
|:- |:- |
|SameAsPrinter|Identisch mit Druckerausrichtung|
|Landschaft|Landschaftsorientierung|
|Porträt|Hochkant|


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(0);

//Set PrintPageOrientation
page.PageSheet.PrintProps.PrintPageOrientation.Value = PrintPageOrientationValue.Landscape;

{{< /highlight >}}


### **Vergößerungsfaktor, Verkleinerungsfaktor**

 Es ist möglich, die Größe einer Seite zu verkleinern oder zu vergrößern, indem Sie den Skalierungsfaktor mit anpassen[**SkalaX**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/scalex)Eigentum.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Set ScaleX and ScaleY
diagram.Pages[0].PageSheet.PrintProps.ScaleX.Value = 1;
diagram.Pages[0].PageSheet.PrintProps.ScaleY.Value = 1;

{{< /highlight >}}

