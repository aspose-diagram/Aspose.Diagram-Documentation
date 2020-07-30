---
title : "Aspose.Diagram for .NET 18.3 Release Notes" 
description : "" 
weight : 12139 
toc : false
type: docs
url: /net/releasenotes/2018/aspose.diagram+for+.net+18.3+release+notes/
---

# Aspose.Diagram for .NET : Aspose.Diagram for .NET 18.3 Release Notes


This page contains release notes for [Aspose.Diagram for .NET 18.3](https://www.nuget.org/packages/Aspose.Diagram/18.3.0).

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMNET-50147|VSD to XPS conversion, the empty pages are created having red cross images|Enhancement|
|DIAGRAMNET-51431|Add MoveTo method for Pages collection|Enhancement|
|DIAGRAMNET-50424  |VSDX to PDF conversion, the icon is overlying the text|Bug|
|DIAGRAMNET-50459|VSDX to PDF conversion, shape icon is misplaced from its original position|Bug|
|DIAGRAMNET-50460|VSDX to PDF conversion, shape icon is misplaced from its original position|Bug|
|DIAGRAMNET-50674|All HTML resources are not saved at the custom path|Bug|
|DIAGRAMNET-51403|VSD to image - the arrow heads are misplaced|Bug|
|DIAGRAMNET-51427|Output VSDX - the controls in Shapes do not work|Bug|
|DIAGRAMNET-51429|Fix Product Page URL over NuGet Gallery|Bug|
|DIAGRAMNET-51432|Open and save routine of VSDX does not preserve font cell|Bug|
|DIAGRAMNET-51433|Cannot retrieve all shape names from a VSDX drawing|Bug|
{{< /table >}}

## Public API and Backwards Incompatible Changes

The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for .NET. If you have concerns about any change listed, please raise them in the [Aspose.Diagram support forum](https://forum.aspose.com/c/diagram).

### Adds MoveTo member in Page class

The MoveTo member takes the target page index as a parameter to move the position of page in the Visio drawing.

{{< code lang="cs" >}}
// import diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page newPage = new Page(1);
// move page in the diagram
newPage.MoveTo(2);
{{< /code >}}

### Usage Examples

Please check the list of help topics added in the Aspose.Diagram Wiki docs: 

1.  [Move Page position in the Visio drawing](https://docs2.aspose.com/diagram/net/developerguide/workingwithpages/retrieve+get+copy+and+insert+a+page#retrieve,get,copyandinsertapage-movepagepositioninthevisiodrawing)

