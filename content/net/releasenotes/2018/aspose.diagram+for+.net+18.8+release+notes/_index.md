---
title : "Aspose.Diagram for .NET 18.8 Release Notes" 
description : "" 
weight : 12134 
toc : false
type: docs
url: /net/releasenotes/2018/aspose.diagram+for+.net+18.8+release+notes/
---

# Aspose.Diagram for .NET : Aspose.Diagram for .NET 18.8 Release Notes


This page contains release notes for [Aspose.Diagram for .NET 18.8](https://www.nuget.org/packages/Aspose.Diagram/18.8.0).

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMNET-51500|Problem rendering to image|Enhancement|
|DIAGRAMNET-51504|Add support to create new reviewer|Enhancement|
|DIAGRAMNET-50953|The text items are displaced on converting a VSDX to PNG|Bug|
|DIAGRAMNET-51122|The incorrect position of text items on converting a VSD to PDF|Bug|
|DIAGRAMNET-51123|The text of the shapes is displaced on converting a VSD to PDF|Bug|
|DIAGRAMNET-51408|VSD to Image - the characters overlap with line|Bug|
|DIAGRAMNET-51499|Diagram.Save method throws OutOfMemoryException|Bug|
|DIAGRAMNET-51501|Shapes are overlapping in VDX file|Bug|
|DIAGRAMNET-51505|Dots missing in generated PDF|Bug|
{{< /table >}}

## Public API and Backwards Incompatible Changes

The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for .NET. If you have concerns about any change listed, please raise them in the [Aspose.Diagram support forum](https://forum.aspose.com/c/diagram).

#### Adds Reviewer

{{< code lang="cs" >}}
            Reviewer viewer = new Reviewer();
            viewer.Name.Value = "test";
            viewer.ReviewerID.Value = 3;
{{< /code >}}

