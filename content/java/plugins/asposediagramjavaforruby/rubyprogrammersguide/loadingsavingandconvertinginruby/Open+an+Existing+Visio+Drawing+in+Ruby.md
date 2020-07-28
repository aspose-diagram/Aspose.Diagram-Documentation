+++
title = "Open an Existing Visio Drawing in Ruby" 
description = "" 
weight = 20103 
+++

Aspose.Diagram for Java : Open an Existing Visio Drawing in Ruby  

# Aspose.Diagram for Java : Open an Existing Visio Drawing in Ruby


## Aspose.Diagram - Open an Existing Visio Drawing

To Open an Existing Visio Drawing using **Aspose.Diagram Java for Ruby**, you can use following code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Call the diagram constructor to load diagram from a VSD filediagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")

