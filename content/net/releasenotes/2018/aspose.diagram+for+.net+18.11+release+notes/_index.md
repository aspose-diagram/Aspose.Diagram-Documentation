---
title : "Aspose.Diagram for .NET 18.11 Release Notes" 
description : "" 
weight : 12131 
toc : false
type: docs
url: /net/releasenotes/2018/aspose.diagram+for+.net+18.11+release+notes/
---

# Aspose.Diagram for .NET : Aspose.Diagram for .NET 18.11 Release Notes


This page contains release notes for [Aspose.Diagram for .NET 18.11](https://www.nuget.org/packages/Aspose.Diagram/18.11.0)

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMNET-50410|MilestoneHelper - Add support of custom date string format setter|Enhancement|
|DIAGRAMNET-51568|Add an option to set ViewBox in SaveOptions for SVG|Enhancement|
|DIAGRAMNET-51580|Aspose.Diagram creates SVG with guidelines and MS Visio does not|Enhancement|
|DIAGRAMNET-51556|Shape.ToImage method is not generating correct images|Bug|
|DIAGRAMNET-51557|Shape.ToImage method returns blank images in case of copy of the page|Bug|
|DIAGRAMNET-51570|Shape.ToImage method is not generating correct images|Bug|
|DIAGRAMNET-51576|VSDX to PDF - Missing Text Blocks|Bug|
|DIAGRAMNET-51578|VSDX to image results in StackOverFlowException|Bug|
{{< /table >}}

## Public API and Backwards Incompatible Changes

The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for .NET. If you have concerns about any change listed, please raise them in the [Aspose.Diagram support forum](https://forum.aspose.com/c/diagram).

### Adds SVGFitToViewPort in SVGSaveOptions

If this property is true, the generated SVG will fit to view port.

{{< code lang="cs" >}}
SVGSaveOptions option = new SVGSaveOptions();
option.SVGFitToViewPort = true;
SVGSaveOptions option = new SVGSaveOptions();
option.SVGFitToViewPort = true;
{{< /code >}}

### Adds ExportGuideShapes in RenderingSaveOptions

Defines whether need exporting the guide shapes or not.

{{< code lang="cs" >}}
Aspose.Diagram.Saving.SVGSaveOptions o = new SVGSaveOptions();
o.ExportGuideShapes = false;
{{< /code >}}

### Adds DateFormatString in MilestoneHelper

DateFormat string of shape

{{< code lang="cs" >}}
milestoneHelper.DateFormatString = "yyyy/mm/dd";
{{< /code >}}

