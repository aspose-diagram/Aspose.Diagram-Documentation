---
title: Appliquer une feuille de style personnalisée à un Visio Diagram en Ruby
type: docs
weight: 10
url: /fr/java/apply-custom-style-sheet-to-a-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Appliquer une feuille de style personnalisée à un Visio Diagram**
 Pour appliquer une feuille de style personnalisée à un Visio Diagram à l'aide**Aspose.Diagram Java pour rubis** , invoquez simplement**ApplyCustomStyleSheet** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

formes = diagram.getPages().getPage(0).getShapes()

je = 0

 alors que je< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process"

        source_shape = shape

        break

    end

    i +=1

end

\# Find the required style sheet

stylesheets = diagram.getStyleSheets()

j = 0

while j < stylesheets.getCount()

    stylesheet = stylesheets.get(j)

    if stylesheet.getName() == "Basic"

        custom_stylesheet = stylesheet

        break

    end

    j +=1

end

if source_shape != nil && custom_stylesheet != nil

    # Apply text style

    source_shape.setTextStyle(custom_stylesheet)

    # Apply fill style

    source_shape.setFillStyle(custom_stylesheet)

    # Apply line style

    source_shape.setLineStyle(custom_stylesheet)

end

\# Save diagram

diagram.save(data_dir + "ApplyCustomStyleSheet.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Applied custom stylesheet to a visio diagram."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Appliquer une feuille de style personnalisée à un Visio Diagram (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/applycustomstylesheet.rb)
