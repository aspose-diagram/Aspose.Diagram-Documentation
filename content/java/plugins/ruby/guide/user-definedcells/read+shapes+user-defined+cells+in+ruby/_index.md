---
title : "Read Shapes User-Defined Cells in Ruby" 
description : "" 
weight : 20158 
toc : false
type: docs
url: /java/plugins/ruby/guide/user-definedcells/read+shapes+user-defined+cells+in+ruby/
---

# Aspose.Diagram for Java : Read Shape's User-Defined Cells in Ruby


## Aspose.Diagram - Read Shape's User-Defined Cells

To Read Shape's User-Defined Cells using **Aspose.Diagram Java for Ruby**, simply invoke **ReadUserDefinedCells** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "UserDefinedCells.vdx")shapes = diagram.getPages().getPage("Flow 1").getShapes()i = 0while i < shapes.getCount()    shape = shapes.get(i)    if shape.getNameU() == "Process"        users = shape.getUsers()        j = 0        while j < users.getCount()            user = users.get(j)            puts user.getName() + ": " + user.getValue().getVal()            j +=1        end        break    end    i +=1end

## Download Running Code

Download **Read Shape's User-Defined Cells (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/readuserdefinedcells.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/UserDefinedCells/readuserdefinedcells.rb)

