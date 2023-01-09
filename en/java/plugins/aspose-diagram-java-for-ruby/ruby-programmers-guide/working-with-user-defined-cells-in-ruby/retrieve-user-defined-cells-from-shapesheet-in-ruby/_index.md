---
title: Retrieve User-defined Cells from Shapesheet in Ruby
type: docs
weight: 30
url: /java/retrieve-user-defined-cells-from-shapesheet-in-ruby/
---

## **Aspose.Diagram - Retrieve User-defined Cells from Shapesheet**
To Retrieve User-defined Cells from Shapesheet using **Aspose.Diagram Java for Ruby**, simply invoke **GetUserDefinedCells** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

pages = diagram.getPages()

count = 0

while count < pages.getCount()

    page = pages.get(count)

    shapes = page.getShapes()

    i = 0

    while i < shapes.getCount()

        shape = shapes.get(i)

        if shape.getNameU() == "Process"

            users = shape.getUsers()

            j = 0

            while j < users.getCount()

                user = users.get(j)

                            puts "Name: " + user.getNameU() + " Value: " + user.getValue().getVal() + " Prompt: " + user.getPrompt().getValue()

                j +=1

            end

            break

        end

        i +=1

    end

    count +=1

end

{{< /highlight >}}
## **Download Running Code**
Download **Retrieve User-defined Cells from Shapesheet (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/getuserdefinedcells.rb)
