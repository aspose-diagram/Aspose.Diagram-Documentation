﻿---
title: Druckoptionen einstellen
type: docs
weight: 10
url: /de/java/setting-print-options/
description: In diesem Abschnitt wird erläutert, wie Sie Druckoptionen mit Aspose.Diagram festlegen.
---
{{% alert color="primary" %}}

Manchmal ist es erforderlich, Seiteneinrichtungseinstellungen für Seiten zu konfigurieren, um den Druck zu steuern. Diese Seiteneinrichtungseinstellungen bieten verschiedene Optionen.

{{% /alert %}}

## **Druckoptionen einstellen**

Seiteneinrichtungsoptionen werden in Aspose.Diagram vollständig unterstützt. Dieser Artikel erläutert, wie Seitenoptionen mit Aspose.Diagram festgelegt werden, und zeigt Codebeispiele für die Einstellung:

 Aspose.Diagram bietet eine Klasse,[**Buchseite**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) , die eine Microsoft Visio-Datei darstellt. Das[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Klasse enthält a[**Seiten**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection) Sammlung, die den Zugriff auf jede Seite in der Datei Visio ermöglicht. Eine Seite wird durch die dargestellt[**Buchseite**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)Klasse.

 Das[**Seitenblatt**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) Klasse bietet die[**PrintRequisiten**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) -Eigenschaft, die zum Festlegen der Seiteneinrichtungsoptionen der Seite verwendet wird. In der Tat dies[**PrintRequisiten**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) Eigentum ist ein Objekt der[**Seitenblatt**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) Klasse zum Festlegen verschiedener Seitenlayoutoptionen für eine gedruckte Seite. Das[**PrintRequisiten**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)-Klasse stellt verschiedene Eigenschaften bereit, die zum Festlegen von Seiteneinrichtungsoptionen verwendet werden. Einige dieser Eigenschaften werden unten diskutiert.

### **Ausrichtung der Druckseite**

 Die Druckseitenausrichtung kann mithilfe von auf Hoch- oder Querformat eingestellt werden[**PrintRequisiten**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) Klasse'[**PrintPageOrientation**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) Eigentum. Das[**PrintPageOrientation**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation) Die Eigenschaft akzeptiert einen der vordefinierten Werte in der[**PrintPageOrientationValue**](https://reference.aspose.com/diagram/java/com.aspose.diagram/PrintPageOrientationValue)Aufzählung, unten aufgeführt.

|**Ausrichtungstypen für Druckseiten**|**Beschreibung**|
|:- |:- |
|SameAsPrinter|Identisch mit Druckerausrichtung|
|Landschaft|Landschaftsorientierung|
|Porträt|Hochkant|

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-SetPageOrientation-SetPageOrientation.java" >}}

### **Vergößerungsfaktor, Verkleinerungsfaktor**

 Es ist möglich, die Größe einer Seite zu verkleinern oder zu vergrößern, indem Sie den Skalierungsfaktor mit anpassen[**SkalaX**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#ScaleX)Eigentum.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-SetPageOrientation-SetPageScale.java" >}}
