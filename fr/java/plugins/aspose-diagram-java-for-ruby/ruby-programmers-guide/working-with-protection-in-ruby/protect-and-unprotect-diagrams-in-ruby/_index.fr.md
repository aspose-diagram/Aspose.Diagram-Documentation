---
title: Protéger et déprotéger les diagrammes en Ruby
type: docs
weight: 20
url: /fr/java/protect-and-unprotect-diagrams-in-ruby/
---
## **Aspose.Diagram - Protéger et déprotéger les diagrammes**
 Pour protéger et déprotéger des diagrammes à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**ProtégerDéprotégerDiagramme** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

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
## **Télécharger le code d'exécution**
 Télécharger**Protéger et déprotéger les diagrammes (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Protection/protectunprotectdiagram.rb)
