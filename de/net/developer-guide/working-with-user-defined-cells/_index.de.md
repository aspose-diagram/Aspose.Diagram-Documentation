---
title: Arbeiten mit benutzerdefinierten Zellen
type: docs
weight: 150
url: /de/net/working-with-user-defined-cells/
description: In diesem Abschnitt wird erläutert, wie benutzerdefinierte Zellen der visio-Formen mit Aspose.Diagram gelesen werden.
---
## **Benutzerdefinierte Zellen der Visio-Formen lesen**
 Benutzer fügen Textfelder in Formen ein, um zusätzliche Informationen anzuzeigen.**Benutzerdefinierte Zellen** ist die eine Verzweigung dieser Felder, und diese Verzweigung verwendet Informationen, die in die Wertzelle des Abschnitts Benutzerdefinierte Zellen im ShapeSheet des Shapes eingegeben wurden. Entwickler können alle benutzerdefinierten Zellen mit einfügen und lesen[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Rufen Sie die benutzerdefinierten Zellenfelder ab**
 Benutzersammlung verfügbar gemacht von[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) -Klasse unterstützt das Objekt Aspose.Diagram.User. Diese Eigenschaft kann verwendet werden, um die benutzerdefinierten Zellen einer Visio-Form zu lesen, wie sie im Abschnitt Benutzerdefinierte Zellen des ShapeSheet der Form verfügbar sind.

![todo: Bild_alt_Text](working-with-user-defined-cells_1.png)
#### **Programmierbeispiel für Zellen abrufen**
Der folgende Codeabschnitt ermöglicht es Entwicklern, die benutzerdefinierten Zellenfelder zu lesen.

```
{{< highlight "csharp" >}}
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
```


Dieses Bild zeigt die Ausgabe nach dem Ausführen des obigen Codes:

![todo: Bild_alt_Text](working-with-user-defined-cells_2.png)
## **Erstellen Sie eine benutzerdefinierte Zelle im ShapeSheet**
[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/) ermöglicht das Erstellen benutzerdefinierter Zellen im Shapesheet. In diesem Beispielthema wird beschrieben, wie Entwickler beliebig viele User.name-Zeilen hinzufügen, den Zeilen aussagekräftige Namen zuweisen und Zellenwerte festlegen können.
### **Benutzerdefinierte Zelle erstellen**
Die Add-Methode, die von der Users Collection verfügbar gemacht wird, kann verwendet werden, um eine benutzerdefinierte Zelle im Shapesheet zu erstellen. Es dauert einen einzigen Parameter.
#### **Beispiel für die Zellprogrammierung erstellen**
Verwenden Sie das folgende Codebeispiel in Ihrer .NET-Anwendung, um eine benutzerdefinierte Zelle im Shapesheet mit Aspose.Diagram for .NET zu erstellen.

```
{{< highlight "csharp" >}}
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
```
## **Benutzerdefinierte Zellen aus Shapesheet abrufen**
Aspose.Diagram for .NET API ermöglicht das Abrufen benutzerdefinierter Zellen aus dem Shapesheet. In diesem Beispielthema wird beschrieben, wie Entwickler alle Benutzernamen für alle Formen in einer Zeichnung abrufen können.
### **Benutzerdefinierte Zellen abrufen**
Die von der User-Klasse bereitgestellten Eigenschaften NameU, Value.Val und Prompt.Value können verwendet werden, um benutzerdefinierte Zellen aus dem Shapesheet abzurufen.
#### **Abrufen von Zellen aus Shapesheet-Programmierbeispielen**
Verwenden Sie den folgenden Code in Ihrer .NET-Anwendung, um alle benutzerdefinierten Zellen aus dem Shapesheet mit Aspose.Diagram for .NET abzurufen.

```
{{< highlight "csharp" >}}
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
```
