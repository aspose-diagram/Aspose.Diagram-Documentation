---
title: Travailler avec des cellules définies par l'utilisateur
type: docs
weight: 100
url: /fr/java/working-with-user-defined-cells/
---
## **Lire les cellules définies par l'utilisateur des formes Visio**
 Les utilisateurs insèrent des champs de texte dans des formes pour afficher des informations supplémentaires.**Cellules définies par l'utilisateur** est la seule branche de ces champs et cette branche utilise les informations saisies dans la cellule Valeur de la section Cellules définies par l'utilisateur dans la feuille ShapeSheet de la forme. Les développeurs peuvent insérer et lire toutes les cellules définies par l'utilisateur à l'aide de[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 La collection Users exposée par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) prend en charge l'objet com.aspose.diagram.User. La[Utilisateur](https://reference.aspose.com/diagram/java/com.aspose.diagram/User) class peut être utilisé pour lire des propriétés. Il existe quelques cellules définies par l'utilisateur, comme vous pouvez le voir dans l'image suivante :

**Tableau affichant des informations sur les cellules définies par l'utilisateur** 

![tâche : image_autre_texte](working-with-user-defined-cells_1.png)

Le code suivant est utilisé pour lire les cellules définies par l'utilisateur.

L'image suivante montre le résultat après l'exécution du code :

![tâche : image_autre_texte](working-with-user-defined-cells_2.png)
#### **Exemples de programmation**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadUserdefinedCellsOfShape.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(1);
// extract user defined cells of the shape
for (User user :(Iterable<User>) shape.getUsers())
{
    System.out.println(user.getName() + ": " + user.getValue().getVal());
}

{{< /highlight >}}
```
### **Créer une cellule définie par l'utilisateur**
Le Aspose.Diagram for Java API permet aux développeurs de créer une cellule définie par l'utilisateur dans la feuille de formes. Cet exemple de rubrique décrit comment ajouter autant de lignes de nom d'utilisateur que nécessaire, attribuer des noms significatifs aux lignes et définir des valeurs de cellule.

La méthode add exposée par la collection Users peut être utilisée pour créer une cellule définie par l'utilisateur dans la feuille de formes. Il prend un seul paramètre.

Utilisez le code suivant dans votre application Java pour créer une cellule définie par l'utilisateur dans la feuille de forme à l'aide de Aspose.Diagram for Java.
#### **Exemples de programmation**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateUserDefinedCellInShapeSheet.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(2);
        
// initialize user object
User user = new User();
user.setName("UserDefineCell");
user.getValue().setVal("800");
// add user-defined cell
shape.getUsers().add(user);

// save diagram
diagram.save(dataDir + "CreateUserDefinedCellInShapeSheet_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Récupérer des cellules définies par l'utilisateur à partir de la feuille de forme**
Aspose.Diagram for Java API permet aux développeurs de récupérer des cellules définies par l'utilisateur à partir de la feuille de formes. Cet exemple de rubrique décrit comment récupérer tous les noms d'utilisateur pour toutes les formes d'un dessin.
### **Récupérer des cellules définies par l'utilisateur**
 Les méthodes getNameU(), getValue().getVal() et getPrompt().getValue() exposées par le[Utilisateur](https://reference.aspose.com/diagram/java/com.aspose.diagram/User)La classe peut être utilisée pour récupérer des cellules définies par l'utilisateur à partir d'une feuille de formes.
#### **Récupérer des cellules à partir d'exemples de programmation de feuille de forme**
Utilisez le code suivant dans votre application Java pour récupérer toutes les cellules définies par l'utilisateur à partir de la feuille de forme à l'aide de Aspose.Diagram for Java.
#### **Exemples de programmation**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateUserDefinedCellInShapeSheet.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(2);
        
// initialize user object
User user = new User();
user.setName("UserDefineCell");
user.getValue().setVal("800");
// add user-defined cell
shape.getUsers().add(user);

// save diagram
diagram.save(dataDir + "CreateUserDefinedCellInShapeSheet_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
