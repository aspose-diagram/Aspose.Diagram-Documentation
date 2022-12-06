---
title: حماية الرسوم البيانية وإلغاء حمايتها في Ruby
type: docs
weight: 20
url: /ar/java/protect-and-unprotect-diagrams-in-ruby/
---
## **Aspose.Diagram - حماية المخططات وإلغاء حمايتها**
 لحماية الرسوم التخطيطية وإلغاء حمايتها باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**ProtectUnprotectDiagram** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

diagram.getDocumentSettings().setProtectBkgnds(1)

diagram.getDocumentSettings().setProtectMasters(1)

diagram.getDocumentSettings().setProtectShapes(1)

diagram.getDocumentSettings().setProtectStyles(1)

\# Save diagram

diagram.save(data_dir + "ProtectUnprotectDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Applied protection on diagram successfully!"

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**حماية الرسوم التخطيطية وإلغاء حمايتها (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Protection/protectunprotectdiagram.rb)
