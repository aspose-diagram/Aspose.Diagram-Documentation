---
title: Travailler avec des commentaires
type: docs
weight: 210
url: /fr/java/working-with-comments/
---
## **Ajouter un commentaire au niveau de la page dans le Visio**
Aspose.Diagram for Java API permet aux développeurs d'ajouter des commentaires n'importe où sur une page du dessin Visio.
### **Ajouter un commentaire**
La méthode addComment, exposée par la classe Page, permet d'ajouter des commentaires à une page de dessin. Il prend les coordonnées X et Y avec une chaîne de commentaire.

 Les utilisateurs Microsoft Visio ajoutent des commentaires à la page entière qui sont présentés par une icône dans le coin supérieur gauche de la page. Les développeurs peuvent[ajouter des commentaires au niveau de la page dans le Visio](). [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API prend également en charge la modification du commentaire au niveau de la page dans le Visio.
#### **Ajouter un commentaire Exemple de programmation**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.java" >}}
## **Modifier un commentaire au niveau de la page dans le Visio Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API prend en charge la modification des commentaires au niveau de la page sur la page de dessin Visio qui sont présentés par une icône dans le coin supérieur gauche de la page.
### **Modifier le commentaire**
La propriété Comment, exposée par la classe Annotation, permet aux développeurs de modifier les commentaires dans la page de dessin Visio.
#### **Éditer un exemple de programmation de commentaire**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.java" >}}
## **Ajouter un commentaire au niveau de la forme dans le dessin Visio**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API permet aux développeurs d'ajouter des commentaires à la forme dans un dessin Visio.
### **Ajouter un commentaire**
Une méthode addComment surchargée, exposée par la classe Page prend une instance de classe Shape et la chaîne de texte du commentaire.
#### **Ajouter un commentaire Exemple de programmation**
**Java**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// retrieve page by name

Page page = diagram.getPages().getPage("Page-1");

// retrieve shape by ID

Shape shape = page.getShapes().getShape(12);

page.addComment(shape, "Hello");

// save diagram

diagram.save("c:\\temp\\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
