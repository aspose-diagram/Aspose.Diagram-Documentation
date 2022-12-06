---
title: Ruby'de bir Visio Şeklini Koruma ve Korumayı Kaldırma
type: docs
weight: 10
url: /tr/java/protect-and-unprotect-a-visio-shape-in-ruby/
---
## **Aspose.Diagram - Bir Visio Şeklini Koruyun ve Korumayı Kaldırın**
 Bir Visio Şeklini Kullanarak Korumak ve Korumasını Kaldırmak İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**Koru Korumasız Şekil** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

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
## **Çalışan Kodu İndir**
 İndirmek**Bir Visio Şeklini Koruma ve Korumayı Kaldırma (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Protection/protectunprotectshape.rb)
