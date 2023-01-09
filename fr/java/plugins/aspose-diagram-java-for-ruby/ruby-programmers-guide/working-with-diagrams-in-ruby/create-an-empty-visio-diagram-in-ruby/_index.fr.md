---
title: Créer un Visio Diagram vide dans Ruby
type: docs
weight: 10
url: /fr/java/create-an-empty-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Créer un Visio Diagram vide**
 Pour créer un Visio Diagram vide en utilisant**Aspose.Diagram Java pour rubis** , invoquez simplement**Créer un diagramme** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new

\# Save as VDX

diagram.save(data_dir + "CreateDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created visio diagram successfully!"

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Créez un Visio Diagram (Aspose.Diagram) vide**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/creatediagram.rb)
