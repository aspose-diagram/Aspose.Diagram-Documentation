---
title: Read Shape's User-Defined Cells in Ruby
type: docs
weight: 20
url: /java/read-shape-s-user-defined-cells-in-ruby/
---

## **Aspose.Diagram - Read Shape's User-Defined Cells**
To Read Shape's User-Defined Cells using **Aspose.Diagram Java for Ruby**, simply invoke **ReadUserDefinedCells** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

shapes = diagram.getPages().getPage("Flow 1").getShapes()

i = 0

while i < shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process"

        users = shape.getUsers()

        j = 0

        while j < users.getCount()

            user = users.get(j)

            puts user.getName() + ": " + user.getValue().getVal()

            j +=1

        end

        break

    end

    i +=1

end

{{< /highlight >}}
## **Download Running Code**
Download **Read Shape's User-Defined Cells (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/readuserdefinedcells.rb)
- [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/UserDefinedCells/readuserdefinedcells.rb)
