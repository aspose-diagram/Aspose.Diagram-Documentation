---
title: Récupérer les éléments de fenêtre du dessin Visio en Ruby
type: docs
weight: 30
url: /fr/java/retrieve-window-elements-from-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Récupérer les éléments de fenêtre du dessin Visio**
 Pour récupérer des éléments de fenêtre à partir du dessin Visio à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**GetWindowElements** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 Les données_dir = File.dirname(File.dirname(File.dirname(File.dirname(__DOSSIER__)))) + '/données/'

\# Créer une instance de Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Dessin.vsd")

fenêtres = diagram.getWindows()

je = 0

 alors que je< windows.getCount()

    window = windows.get(i)

    puts "ID: " + window.getID().to_s

    puts "Type: " + window.getWindowType().to_s

    puts "Window height: " + window.getWindowHeight().to_s

    puts "Window width: " + window.getWindowWidth().to_s

    puts "Window state: " + window.getWindowState().to_s

    i +=1

end

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Récupérer des éléments de fenêtre à partir du dessin Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/WindowElements/getwindowelements.rb)
