---
title: Travailler avec des cellules définies par l'utilisateur
type: docs
weight: 150
url: /fr/net/working-with-user-defined-cells/
description: Cette section explique comment lire les cellules définies par l'utilisateur des formes visio avec Aspose.Diagram.
---
## **Lire les cellules définies par l'utilisateur des formes Visio**
 Les utilisateurs insèrent des champs de texte dans des formes pour afficher des informations supplémentaires.**Cellules définies par l'utilisateur** est la seule branche de ces champs et cette branche utilise les informations saisies dans la cellule Valeur de la section Cellules définies par l'utilisateur dans la feuille ShapeSheet de la forme. Les développeurs peuvent insérer et lire toutes les cellules définies par l'utilisateur à l'aide de[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Récupérer les champs de cellules définis par l'utilisateur**
 Collection d'utilisateurs exposée par[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) prend en charge l'objet Aspose.Diagram.User. Cette propriété peut être utilisée pour lire les cellules définies par l'utilisateur d'une forme Visio telles que disponibles dans la section Cellules définies par l'utilisateur de la feuille ShapeSheet de la forme.

![tâche : image_autre_texte](working-with-user-defined-cells_1.png)
#### **Exemple de programmation de récupération de cellules**
Le morceau de code suivant permet aux développeurs de lire les champs de cellules définis par l'utilisateur.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UserDefinedCells();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(1);
// Extract user defined cells of the shape
foreach (User user in shape.Users)
{
    Console.WriteLine(user.Name + ": " + user.Value.Val);
}

{{< /highlight >}}



Cette image montre la sortie après avoir exécuté le code ci-dessus :

![tâche : image_autre_texte](working-with-user-defined-cells_2.png)
## **Créer une cellule définie par l'utilisateur dans la feuille ShapeSheet**
[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/) permet de créer une cellule définie par l'utilisateur dans la feuille de formes. Cet exemple de rubrique décrit la façon dont les développeurs peuvent ajouter autant de lignes User.name qu'ils en ont besoin, attribuer des noms significatifs aux lignes et définir des valeurs de cellule.
### **Créer une cellule définie par l'utilisateur**
La méthode Add exposée par la collection Users peut être utilisée pour créer une cellule définie par l'utilisateur dans la feuille de formes. Il prend un seul paramètre.
#### **Créer un exemple de programmation de cellule**
Utilisez l'exemple de code suivant dans votre application .NET pour créer une cellule définie par l'utilisateur dans la feuille de forme à l'aide de Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UserDefinedCells();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(2);
            
// Initialize user object
User user = new User();
user.Name = "UserDefineCell";
user.Value.Val = "800";
// Add user-defined cell
shape.Users.Add(user);

// Save diagram
diagram.Save(dataDir + "CreateUserDefinedCellInShapeSheet_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Récupérer des cellules définies par l'utilisateur à partir de la feuille de forme**
Aspose.Diagram for .NET API permet de récupérer des cellules définies par l'utilisateur à partir d'une feuille de formes. Cet exemple de rubrique décrit la manière dont les développeurs peuvent récupérer tous les User.name pour toutes les formes d'un dessin.
### **Récupérer des cellules définies par l'utilisateur**
Les propriétés NameU, Value.Val et Prompt.Value exposées par la classe User peuvent être utilisées pour récupérer des cellules définies par l'utilisateur à partir d'une feuille de formes.
#### **Récupérer des cellules à partir d'exemples de programmation de feuille de forme**
Utilisez le code suivant dans votre application .NET pour récupérer toutes les cellules définies par l'utilisateur à partir de la feuille de forme à l'aide de Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UserDefinedCells();
int count = 0;
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Iterate through pages
foreach (Aspose.Diagram.Page objPage in diagram.Pages)
{
    // Iterate through shapes
    foreach (Aspose.Diagram.Shape objShape in objPage.Shapes)
    {
        Console.WriteLine(objShape.NameU);
        // Iterate through user-defined cells
        foreach (Aspose.Diagram.User objUserField in objShape.Users)
        {
            count++;
            Console.WriteLine(count + " - Name: " + objUserField.NameU + " Value: " + objUserField.Value.Val + " Prompt: " + objUserField.Prompt.Value);
        }
    }
}  

{{< /highlight >}}

