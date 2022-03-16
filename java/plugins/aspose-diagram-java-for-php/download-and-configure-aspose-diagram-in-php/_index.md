---
title: Download and Configure Aspose.Diagram in PHP
type: docs
weight: 10
url: /java/download-and-configure-aspose-diagram-in-php/
---

## **Download Required Libraries**
Download required libraries mentioned below. These are the required for executing Aspose.Diagram Java for Ruby examples.

- [Aspose.Diagram for Java Component](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram)
## **Download Examples from Social Coding Sites**
Following releases of running examples are available to download on below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/tree/master/Plugins/Aspose_Diagram_Java_for_PHP)
## **Installing**
It is very simple and easy to install Aspose.Diagram Java for PHP, please follow the instructions:

Run following command.

{{< highlight java >}}

 $ gem install asposediagramjava

{{< /highlight >}}
## **Using**
Include the required files to export visio drawing to Pdf document.

{{< highlight java >}}

 require File.dirname(File.dirname(File.dirname(__FILE__))) + '/lib/asposediagramjava'

include Asposediagramjava

include Asposediagramjava::ExportToPdf

initialize_aspose_Diagram

{{< /highlight >}}

Let's understand the above code.

1. The first line makes sure that the Aspose.Diagram is loaded and available.
1. Include the files that are required to access the Aspose.Diagram
1. Initialize the libraries. The aspose Java classes are loaded from the path provided in the aspose.yml file
