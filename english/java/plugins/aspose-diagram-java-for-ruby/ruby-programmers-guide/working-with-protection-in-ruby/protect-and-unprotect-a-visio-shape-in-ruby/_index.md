---
title: Protect and Unprotect a Visio Shape in Ruby
type: docs
weight: 10
url: /java/protect-and-unprotect-a-visio-shape-in-ruby/
---

## **Aspose.Diagram - Protect and Unprotect a Visio Shape**
To Protect and Unprotect a Visio Shape using **Aspose.Diagram Java for Ruby**, simply invoke **ProtectUnprotectShape** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

page = diagram.getPages().getPage("Flow 1")

shape = page.getShapes().getShape(1)

shape.getProtection().getLockAspect().setValue(1)

shape.getProtection().getLockBegin().setValue(1)

shape.getProtection().getLockCalcWH().setValue(1)

shape.getProtection().getLockCrop().setValue(1)

shape.getProtection().getLockCustProp().setValue(1)

shape.getProtection().getLockDelete().setValue(1)

shape.getProtection().getLockEnd().setValue(1)

shape.getProtection().getLockFormat().setValue(1)

shape.getProtection().getLockFromGroupFormat().setValue(1)

shape.getProtection().getLockGroup().setValue(1)

shape.getProtection().getLockHeight().setValue(1)

shape.getProtection().getLockMoveX().setValue(1)

shape.getProtection().getLockMoveY().setValue(1)

shape.getProtection().getLockRotate().setValue(1)

shape.getProtection().getLockSelect().setValue(1)

shape.getProtection().getLockTextEdit().setValue(1)

shape.getProtection().getLockThemeColors().setValue(1)

shape.getProtection().getLockThemeEffects().setValue(1)

shape.getProtection().getLockVtxEdit().setValue(1)

shape.getProtection().getLockWidth().setValue(1)

\# Save diagram

diagram.save(data_dir + "ProtectUnprotectShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Applied protection on shape successfully!"

{{< /highlight >}}
## **Download Running Code**
Download **Protect and Unprotect a Visio Shape (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Protection/protectunprotectshape.rb)
