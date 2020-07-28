+++
title = "Aspose.Diagram for Java 19.11 Release Notes" 
description = "" 
weight = 12251 
+++

Aspose.Diagram for Java : Aspose.Diagram for Java 19.11 Release Notes  

# Aspose.Diagram for Java : Aspose.Diagram for Java 19.11 Release Notes


This page contains release notes information for Aspose.Diagram for Java 19.11.

## Improvements and Changes

This month's release allows formatting Visio pages by [applying stylesheets](https://docs2.aspose.com/diagram/java/developerguide/workingwithpages/format+visio+pages).

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|DIAGRAMJAVA-50671|Shape sheet new window setting not respected when converting to SVG|Enhancement|
{{< /table >}}

### **Public API and Backwards Incompatible Changes**

The following is a list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for JAVA. If you have concerns about any change listed, please raise it on the Aspose.Diagram support forum.

### Added applyStyle in Page

{{< code lang="cs" >}}
StyleSheet st = new StyleSheet();
dia.getPages().get(0).applyStyle(st.ID, st.ID, st.ID);
{{< /code >}}

###  Added dispose in Diagram class

Performs application-defined tasks associated with freeing, releasing, or resetting unmanaged resources.

diagram.dispose();

