---
title: Aspose.Diagram for Java 18.8 Release Notes
type: docs
weight: 50
url: /java/aspose-diagram-for-java-18-8-release-notes/
---

{{% alert color="primary" %}} 

This page contains release notes for [Aspose.Diagram for Java 18.8](https://repository.aspose.com/repo/com/aspose/aspose-diagram/18.8/).

{{% /alert %}} 
## **Improvements and Changes**

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|DIAGRAMJAVA-50611|Support for Setting locale with the API|Enhancement|
|DIAGRAMJAVA-50606|VSDX to SVG - incorrect rendering of the arrows|Bug|
|DIAGRAMJAVA-50610|Location of Text on Connectors is wrong in output VSDX file|Bug|
|DIAGRAMJAVA-50612|Unable to open output VDX file with Visio Viewer 2010 Professional|Bug|
## **Public API and Backwards Incompatible Changes**
The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for Java. If you have concerns about any change listed, please raise them in the [Aspose.Diagram support forum](https://forum.aspose.com/c/diagram).
#### **Added setLocale in LoadOption**
{{< highlight java >}}

         LoadOptions loadOptions = new LoadOptions( LoadFileFormat.VDX ); 

        loadOptions.setLocale(Locale.US);

        Diagram diagram = new Diagram("test.vdx", loadOptions); 

{{< /highlight >}}

sets the Locale used for diagram at the time the file was loaded.
