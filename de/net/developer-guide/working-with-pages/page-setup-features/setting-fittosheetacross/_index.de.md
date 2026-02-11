---
title: Einstellen von FitToSheetAcross
type: docs
weight: 10
url: /de/net/setting-fittosheetacross/
description: In diesem Abschnitt wird erläutert, wie Sie fittosheetacross mit Aspose.Diagram einstellen.
---
{{% alert color="primary" %}}

Manchmal ist es erforderlich, Seiteneinrichtungseinstellungen für Seiten zu konfigurieren, um den Druck zu steuern. Diese Seiteneinrichtungseinstellungen bieten verschiedene Optionen.

{{% /alert %}}

## **Einstellen von FitToSheetAcross**

Seiteneinrichtungsoptionen werden in Aspose.Diagram vollständig unterstützt. Dieser Artikel erläutert, wie Seitenoptionen mit Aspose.Diagram festgelegt werden, und zeigt Codebeispiele für die Einstellung:

 Aspose.Diagram bietet eine Klasse,[**Buchseite**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , die eine Microsoft Visio-Datei darstellt. Das[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) Klasse enthält a[**Seiten**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) Sammlung, die den Zugriff auf jede Seite in der Datei Visio ermöglicht. Eine Seite wird durch die dargestellt[**Buchseite**](https://reference.aspose.com/diagram/net/aspose.diagram/page)Klasse.

 Das[**Seitenblatt**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) Klasse bietet die[**PrintRequisiten**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) -Eigenschaft, die zum Festlegen der Seiteneinrichtungsoptionen der Seite verwendet wird. In der Tat dies[**PrintRequisiten**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) Eigentum ist ein Objekt der[**Seitenblatt**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) Klasse zum Festlegen verschiedener Seitenlayoutoptionen für eine gedruckte Seite. Das[**PrintRequisiten**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)-Klasse stellt verschiedene Eigenschaften bereit, die zum Festlegen von Seiteneinrichtungsoptionen verwendet werden. Einige dieser Eigenschaften werden unten diskutiert.

### **FitToSheetAcross**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

PrintProps printProps = diagram.Pages[0].PageSheet.PrintProps;

printProps.OnPage.Value = BOOL.True;

//Set Fit to sheet(s) across
printProps.PagesX.Value = 1;

//Set By sheet(s) down
printProps.PagesY.Value = 1;

{{< /highlight >}}



