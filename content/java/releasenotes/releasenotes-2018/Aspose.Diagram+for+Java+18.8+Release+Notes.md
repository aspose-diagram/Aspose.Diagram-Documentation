+++
title = "Aspose.Diagram for Java 18.8 Release Notes" 
description = "" 
weight = 12267 
+++

Aspose.Diagram for Java : Aspose.Diagram for Java 18.8 Release Notes  

# Aspose.Diagram for Java : Aspose.Diagram for Java 18.8 Release Notes


This page contains release notes for [Aspose.Diagram for Java 18.8](https://repository.aspose.com/repo/com/aspose/aspose-diagram/18.8/).

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMJAVA-50611|Support for Setting locale with the API|Enhancement|
|DIAGRAMJAVA-50606|VSDX to SVG - incorrect rendering of the arrows|Bug|
|DIAGRAMJAVA-50610|Location of Text on Connectors is wrong in output VSDX file|Bug|
|DIAGRAMJAVA-50612|Unable to open output VDX file with Visio Viewer 2010 Professional|Bug|
{{< /table >}}

## Public API and Backwards Incompatible Changes

The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for Java. If you have concerns about any change listed, please raise them in the [Aspose.Diagram support forum](https://forum.aspose.com/c/diagram).

#### Added setLocale in LoadOption

{{< code lang="cs" >}}
        LoadOptions loadOptions = new LoadOptions( LoadFileFormat.VDX ); 
        loadOptions.setLocale(Locale.US);
        Diagram diagram = new Diagram("test.vdx", loadOptions); 
{{< /code >}}

sets the Locale used for diagram at the time the file was loaded.

