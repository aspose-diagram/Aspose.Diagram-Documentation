---
title: Trabajar con celdas definidas por el usuario
type: docs
weight: 150
url: /es/net/working-with-user-defined-cells/
description: Esta sección explica cómo leer las celdas definidas por el usuario de las formas visio con Aspose.Diagram.
---
## **Leer celdas definidas por el usuario de las formas Visio**
 Los usuarios insertan campos de texto en formas para mostrar información adicional.**Celdas definidas por el usuario** es la única rama de estos campos y esta rama utiliza la información ingresada en la celda Valor de la sección Celdas definidas por el usuario en la ShapeSheet de la forma. Los desarrolladores pueden insertar y leer todas las celdas definidas por el usuario usando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Recuperar los campos de celdas definidos por el usuario**
 Colección de usuarios expuesta por[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La clase admite el objeto Aspose.Diagram.User. Esta propiedad se puede usar para leer las celdas definidas por el usuario de una forma Visio disponibles en la sección Celdas definidas por el usuario de ShapeSheet de la forma.

![todo:imagen_alternativa_texto](working-with-user-defined-cells_1.png)
#### **Recuperar muestra de programación de celdas**
El siguiente fragmento de código permite a los desarrolladores leer los campos de las celdas definidas por el usuario.

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


Esta imagen muestra el resultado después de ejecutar el código anterior:

![todo:imagen_alternativa_texto](working-with-user-defined-cells_2.png)
## **Crear celda definida por el usuario en ShapeSheet**
[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/) permite crear celdas definidas por el usuario en la hoja de formas. Este tema de ejemplo describe la forma en que los desarrolladores pueden agregar tantas filas User.name como necesiten, asignar nombres significativos a las filas y establecer valores de celda.
### **Crear celda definida por el usuario**
El método Agregar expuesto por la Colección de usuarios se puede usar para crear una celda definida por el usuario en la hoja de formas. Toma un solo parámetro.
#### **Crear muestra de programación celular**
Use el siguiente ejemplo de código en su aplicación .NET para crear una celda definida por el usuario en la hoja de formas usando Aspose.Diagram for .NET.

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
## **Recuperar celdas definidas por el usuario de Shapesheet**
Aspose.Diagram for .NET API permite recuperar celdas definidas por el usuario de la hoja de forma. Este tema de ejemplo describe la forma en que los desarrolladores pueden recuperar todos los User.name para todas las formas en un dibujo.
### **Recuperar celdas definidas por el usuario**
Las propiedades NameU, Value.Val y Prompt.Value expuestas por la clase User se pueden usar para recuperar celdas definidas por el usuario de la hoja de forma.
#### **Recuperar celdas de muestras de programación de Shapesheet**
Use el siguiente código en su aplicación .NET para recuperar todas las celdas definidas por el usuario de la hoja de formas usando Aspose.Diagram for .NET.

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
