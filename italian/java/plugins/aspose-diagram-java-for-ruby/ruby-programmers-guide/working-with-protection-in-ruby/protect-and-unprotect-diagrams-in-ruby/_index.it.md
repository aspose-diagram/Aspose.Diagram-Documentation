---
title: Proteggere e rimuovere la protezione dei diagrammi in Ruby
type: docs
weight: 20
url: /it/java/protect-and-unprotect-diagrams-in-ruby/
---
## **Aspose.Diagram - Proteggi e sproteggi diagrammi**
 Per proteggere e rimuovere la protezione dei diagrammi utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**ProtectUnprotectDiagram** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

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
## **Scarica il codice in esecuzione**
 Scarica**Diagrammi di protezione e rimozione della protezione (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Protection/protectunprotectdiagram.rb)
