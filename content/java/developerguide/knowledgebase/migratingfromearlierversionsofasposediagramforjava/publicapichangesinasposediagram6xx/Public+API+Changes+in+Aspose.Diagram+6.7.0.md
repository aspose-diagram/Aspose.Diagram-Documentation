+++
title = "Public API Changes in Aspose.Diagram 6.7.0" 
description = "" 
weight = 20075 
+++

Aspose.Diagram for Java : Public API Changes in Aspose.Diagram 6.7.0  

# Aspose.Diagram for Java : Public API Changes in Aspose.Diagram 6.7.0


This document describes changes to the Aspose.Diagram API from version 6.6.0 to 6.7.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram. 

### Adds detectFileFormat method in FileFormatUtil class

It detects and returns the information about the format of a stored Visio diagram in an input stream. Please check this code example:

**Java**

String dataDir = "c:\\\\temp\\\\";// Open the stream. Read only access to load a Visio diagram.InputStream stream = new FileInputStream(dataDir + "Drawing1.vsdx");// detect file format using an input streamFileFormatInfo info = FileFormatUtil.detectFileFormat(stream);// get the detected file formatSystem.out.println("The spreadsheet format is: " + info.getFileFormatType());

