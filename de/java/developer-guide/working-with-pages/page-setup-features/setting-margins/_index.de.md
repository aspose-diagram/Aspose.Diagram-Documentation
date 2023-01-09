﻿---
title: Ränder einstellen
type: docs
weight: 20
url: /de/java/setting-margins/
description: In diesem Abschnitt wird erläutert, wie Sie die Seitenoptionen von visio mit Aspose.Diagram festlegen.
---
{{% alert color="primary" %}}

Aspose.Diagram unterstützt die Seiteneinrichtungsoptionen von Microsoft Visio vollständig. Entwickler müssen möglicherweise Seiteneinrichtungseinstellungen für Seiten konfigurieren, um den Druckprozess zu steuern. In diesem Thema wird erläutert, wie Sie Aspose.Diagram verwenden, um Seitenränder zu konfigurieren.

{{% /alert %}}

## **Ränder einstellen**

 Aspose.Diagram bietet eine Klasse,[**Buchseite**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) , die eine Microsoft Visio-Datei darstellt. Das[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Klasse enthält a[**Seiten**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection) Sammlung, die den Zugriff auf jede Seite in der Datei Visio ermöglicht. Eine Seite wird durch die dargestellt[**Buchseite**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)Klasse.

 Das[**Seitenblatt**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) Klasse bietet die[**PrintRequisiten**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) -Eigenschaft, die zum Festlegen der Seiteneinrichtungsoptionen der Seite verwendet wird. In der Tat dies[**PrintRequisiten**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) Eigentum ist ein Objekt der[**Seitenblatt**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) Klasse zum Festlegen verschiedener Seitenlayoutoptionen für eine gedruckte Seite. Das[**PrintRequisiten**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)-Klasse stellt verschiedene Eigenschaften bereit, die zum Festlegen von Seiteneinrichtungsoptionen verwendet werden. Einige dieser Eigenschaften werden unten diskutiert.

### **Seitenränder**

 Stellen Sie die Seitenränder (PageTopMargin, PageBottomMargin, PageLeftMargin, PageRightMargin) mit ein[**PrintRequisiten**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)Klassenmitglieder. Nachfolgend sind einige der Methoden aufgeführt, die zum Festlegen von Seitenrändern verwendet werden:

- [**PageTopMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageTopMargin)
- [**Seitenunterer Rand**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageBottomMargin)
- [**Linker Seitenrand**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageLeftMargin)
- [**SeiteRightMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageRightMargin)


{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-SetPageMargin-SetPageMargin.java" >}}