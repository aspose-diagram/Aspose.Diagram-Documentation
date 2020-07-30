---
title : "Saving Visio Document in Ruby" 
description : "" 
weight : 20104 
toc : false
type: docs
url: /java/plugins/ruby/guide/ld-sv-cvtinruby/saving+visio+document+in+ruby/
---

# Aspose.Diagram for Java : Saving Visio Document in Ruby


## Aspose.Diagram - Saving Visio Document

To Save Visio Document using **Aspose.Diagram Java for Ruby**, you can use following code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Save as VDXdiagram.save(data\_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

