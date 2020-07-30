---
title : "Aspose.Diagram for .NET 19.9 Release Notes" 
description : "" 
weight : 12120 
toc : false
type: docs
url: /net/releasenotes/2019/aspose.diagram+for+.net+19.9+release+notes/
---

# Aspose.Diagram for .NET : Aspose.Diagram for .NET 19.9 Release Notes


This page contains release notes information for Aspose.Diagram for .NET 19.9.

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMNET-51683|Visio to HTML - Link in generated HTML does not work correctly|Enhancement|
|DIAGRAMNET-51684|While removing unused master shapes and styles only the image has a problem|Enhancement|
|DIAGRAMNET-51711|Unable to add macros after conversion|Enhancement|
|DIAGRAMNET-50383|Reduce the size of Visio diagram|Bug|
|DIAGRAMNET-51682|Get font style from the Diagram|Bug|
|DIAGRAMNET-51685|Visio to SVG - an exception occurs|Bug|
|DIAGRAMNET-51686|Visio to PNG - Output file has unwanted image and shapes|Bug|
|DIAGRAMNET-51687|Visio to PDF - background color of text is absent in output PDF|Bug|
|DIAGRAMNET-51688|Visio to PDF - Color of Shape Frames is different in output|Bug|
|DIAGRAMNET-51689|Visio to JPG - output image is not in correct format|Bug|
|DIAGRAMNET-51691|Visio to PDF - Some shapes are not correct|Bug|
|DIAGRAMNET-51692|Visio to PDF - Some shapes are not correct|Bug|
|DIAGRAMNET-51693|Visio to PDF - Some shapes are not correct|Bug|
|DIAGRAMNET-51694|Visio to PDF - Some shapes are not correct|Bug|
|DIAGRAMNET-51697|Visio to PDF - Some shapes are not correct|Bug|
|DIAGRAMNET-51700|Visio to PDF - Some shapes/lines are not correct|Bug|
|DIAGRAMNET-51702|Visio to PDF - Some shapes/lines are not correct|Bug|
|DIAGRAMNET-51706|Visio to PDF - Some shapes/lines are not correct|Bug|
|DIAGRAMNET-51707|Visio to PDF - Some shapes/lines are not correct|Bug|
|DIAGRAMNET-51708|Visio to PDF - Some shapes/lines are not correct|Bug|
|DIAGRAMNET-51709|Visio to PDF - Some shapes/lines are not correct|Bug|
|DIAGRAMNET-51710|Visio to PDF - Some shapes/lines are not correct|Bug|
{{< /table >}}

### **Public API and Backwards Incompatible Changes**

The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for .NET. If you have concerns about any change listed, please raise it on the Aspose.Diagram support forum.

{{< table style="table-striped" >}}
|Change|Purpose|Sample|
|:----|:----|:----|
|Addition of **IsBold** to Aspose.Shape.Char|Indicating whether the font is bold.|Aspose.Diagram.Char ch = shape.Chars\[0\];|
|ch.IsBold|Addition of **IsItalic** to Aspose.Shape.Char|Indicating whether the font is italic.|
|Aspose.Diagram.Char ch = shape.Chars\[0\];|ch.IsItalic|Addition of **IsUnderline** to Aspose.Shape.Char|
|Indicating whether the font is Underline.|Aspose.Diagram.Char ch = shape.Chars\[0\];|ch.IsUnderline|
|Addition of **IsDoubleUnderline** to Aspose.Shape.Char|Indicating whether the font is Double Underlined|Aspose.Diagram.Char ch = shape.Chars\[0\];|
|ch.IsDoubleUnderline|Addition of **IsStrikethrough** to Aspose.Shape.Char|Indicating whether the font is strikethrough.|
{{< /table >}}

Aspose.Diagram.Char ch = shape.Chars\[0\]

ch.IsStrikethrough 

Addition of **IsDoubleStrikethrough** to Aspose.Shape.Char

Indicating whether the font is Double Strikethrough

Aspose.Diagram.Char ch = shape.Chars\[0\];

ch.IsDoubleStrikethrough

