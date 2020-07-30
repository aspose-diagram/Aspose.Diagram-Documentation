---
title : "Download and Configure Aspose.Diagram in PHP" 
description : "" 
weight : 12169 
toc : false
type: docs
url: /java/plugins/php/download+and+configure+aspose.diagram+in+php/
---

# Aspose.Diagram for Java : Download and Configure Aspose.Diagram in PHP


## **Download Required Libraries**

Download required libraries mentioned below. These are the required for executing Aspose.Diagram Java for Ruby examples.

*   [Aspose.Diagram for Java Component](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-diagram/)

## **Download Examples from Social Coding Sites**

Following releases of running examples are available to download on below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/tree/master/Plugins/Aspose_Diagram_Java_for_PHP)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/)

## **Installing**

It is very simple and easy to install Aspose.Diagram Java for PHP, please follow the instructions:

Run following command.

{{< code lang="cs" >}}
$ gem install asposediagramjava
{{< /code >}}

## **Using**

Include the required files to export visio drawing to Pdf document.

{{< code lang="cs" >}}
require File.dirname(File.dirname(File.dirname(__FILE__))) + '/lib/asposediagramjava'
include Asposediagramjava
include Asposediagramjava::ExportToPdf

initialize_aspose_Diagram
{{< /code >}}

Let's understand the above code.

1.  The first line makes sure that the Aspose.Diagramis loaded and available.
2.  Include the files that are required to access the Aspose.Diagram
3.  Initialize the libraries. The aspose Java classes are loaded from the path provided in the aspose.yml file

