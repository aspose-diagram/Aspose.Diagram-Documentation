+++
title = "Aspose.Diagram for .NET 6.3.0 Release Notes" 
description = "" 
weight = 12164 
+++

Aspose.Diagram for .NET : Aspose.Diagram for .NET 6.3.0 Release Notes  

# Aspose.Diagram for .NET : Aspose.Diagram for .NET 6.3.0 Release Notes


## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMNET-50739|Add support of detecting the Visio diagram type.|New Feature|
|DIAGRAMNET-50746|Prevent export of the hidden Visio pages in the PDF.|New Feature|
|DIAGRAMNET-50747|Prevent export of the hidden Visio pages in the HTML.|New Feature|
|DIAGRAMNET-50750|Prevent export of the hidden Visio pages in the PNG.|New Feature|
|DIAGRAMNET-50751|Prevent export of the hidden Visio pages in the JPEG.|New Feature|
|DIAGRAMNET-50752|Prevent export of the hidden Visio pages in the SVG.|New Feature|
|DIAGRAMNET-50753|Prevent export of the hidden Visio pages in the GIF.|New Feature|
|DIAGRAMNET-50754|Prevent export of the hidden Visio pages in the XPS.|New Feature|
|DIAGRAMNET-50541|VSDX to PDF conversion, Hebrew text items are rendered in reverse order.|Enhancement|
|DIAGRAMNET-50542|VSD to PDF conversion, Arabic word turns into letters.|Enhancement|
|DIAGRAMNET-50682|VSD to PDF export, the table cell's text is partially invisible.|Bug|
|DIAGRAMNET-50712|VDX to PDF export - the text of various shapes is misplaced.|Bug|
|DIAGRAMNET-50741|VSD to SVG export is missing some Visio shapes.|Bug|
|DIAGRAMNET-50742|VSD to SVG export is not applying the inner white color of shapes.|Bug|
|DIAGRAMNET-50744|Open and save routine of VSDX has changed text into dummy characters.|Bug|
|DIAGRAMNET-50745|Open and save routine of VSDX has changed the dotted line shaper.|Bug|
|DIAGRAMNET-50748|VSD to PDF export - the text items are misplaced.|Bug|
|DIAGRAMNET-50763|VSD to VDX export is throwing the Master element error.|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list for any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for .NET. If you have concerns about any change listed, please raise it on the [Aspose.Diagram support forum](http://www.aspose.com/community/forums/aspose.diagram-product-family/489/showforum.aspx).

#### Add FileFormatUtil and FileFormatInfo Classes

These classes give programmatic access to detect the Visio file type.

#### Adds DetectFileFormat Method in FileFormatUtil Class

It detects and returns the information about the format of a stored Visio diagram in a file.

#### Adds FileFormatType Property in FileFormatInfo Class

It gets the detected file format.

#### Adds LoadFormat Property in FileFormatInfo

It gets the detected load format.

#### Adds ExportHiddenPage Property in SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions and PdfSaveOptions Classes

It defines whether need to export the hidden Visio pages or not.

### Usage Examples

Please check the list of help topics added in the Aspose.Diagram Wiki docs:

*   [Control the Export of Hidden Visio Pages on Saving](http://www.aspose.com/docs/display/diagramnet/Set+Orientation+and+Control+the+Export+of+Hidden+Visio+Pages+on+Saving#SetOrientationandControltheExportofHiddenVisioPagesonSaving-ControltheExportofHiddenVisioPagesonSaving)
*   [Detect the Format of Visio File](http://www.aspose.com/docs/display/diagramnet/Introduction#Introduction-DetecttheFormatofVisioFile)

