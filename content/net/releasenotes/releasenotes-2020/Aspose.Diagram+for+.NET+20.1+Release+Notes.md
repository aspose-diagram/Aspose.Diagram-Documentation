+++
title = "Aspose.Diagram for .NET 20.1 Release Notes" 
description = "" 
weight = 12115 
+++

Aspose.Diagram for .NET : Aspose.Diagram for .NET 20.1 Release Notes  

# Aspose.Diagram for .NET : Aspose.Diagram for .NET 20.1 Release Notes


This page contains release notes information for Aspose.Diagram for .NET 20.1.

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMNET-51198|Shade on hyperlink button is not rendered correctly on saving VSDM to SVG|Enhancement|
| DIAGRAMNET-51526|VSDX to PDF - Gradient fill for arrowheads lost in resultant PDF|Enhancement|
|DIAGRAMNET-51539|The gradient in shapes has lost in output SVG|Enhancement|
|DIAGRAMNET-50705|VSD to SVG export - Meta type shapes turn into messy symbols|Bug|
|DIAGRAMNET-51664|File is getting corrupted after removing unused theme|Bug|
|DIAGRAMNET-51665|Images are shown as X after removing unused themes|Bug|
|DIAGRAMNET-51684|While removing unused master shapes and styles only the image has a problem|Bug|
|DIAGRAMNET-51726|Background Image Missing (PowerPoint is added in the VISIO) while removing unused master shapes and styles|Bug|
|DIAGRAMNET-51737|Visio to Html - image size Issue|Bug|
|DIAGRAMNET-51743|Removing private information from Visio - the Visio document size issue|Bug|
|DIAGRAMNET-51745|Strange Error Occurs in WPF application when converting VSD to VSDX|Bug|
{{< /table >}}

## Public API and Backward Incompatible Changes

*   Added Pages to LoadOptions - Specifies the index of the pages to be loaded.

{{< code lang="cs" >}}
Aspose.Diagram.LoadOptions options = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);
options.Pages = new ArrayList();
options.Pages.Add(0);
{{< /code >}}

*   Added SetFontSources in FontConfigs - Sets the Fonts Sources

{{< code lang="cs" >}}
Aspose.Diagram.MemoryFontSource sc1 = new Aspose.Diagram.MemoryFontSource(b);
Aspose.Diagram.MemoryFontSource sc2 = new Aspose.Diagram.MemoryFontSource(b);
Aspose.Diagram.MemoryFontSource[] sc = new Aspose.Diagram.MemoryFontSource[] { sc1, sc2 };
Aspose.Diagram.FontConfigs.SetFontSources(sc); 
{{< /code >}}

