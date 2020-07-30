---
title : "Create User-defined Cell in the ShapeSheet in Ruby" 
description : "" 
weight : 20157 
toc : false
type: docs
url: /java/plugins/ruby/guide/user-definedcells/create+user-defined+cell+in+the+shapesheet+in+ruby/
---

# Aspose.Diagram for Java : Create User-defined Cell in the ShapeSheet in Ruby


## Aspose.Diagram - Create User-defined Cell in the ShapeSheet

To Create User-defined Cell in the ShapeSheet using **Aspose.Diagram Java for Ruby**, simply invoke **CreateUserDefinedCell** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")pages = diagram.getPages()i = 0while i < pages.getCount()    page = pages.get(i)    shapes = page.getShapes()    j = 0    while j < shapes.getCount()        shape = shapes.get(j)        if shape.getNameU() == "Process"            # Initialize user object            user = Rjb::import('com.aspose.diagram.User').new            user.setName("UserDefineCell")            user.getValue().setVal("800")            # Add user-defined cell            shape.getUsers().add(user)        end        j +=1    end    i +=1end# Save diagramdiagram.save(data\_dir + "UserDefinedCells.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Created User-defined Cell in the ShapeSheet."

## Download Running Code

Download **Create User-defined Cell in the ShapeSheet (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/createuserdefinedcell.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/UserDefinedCells/createuserdefinedcell.rb)

