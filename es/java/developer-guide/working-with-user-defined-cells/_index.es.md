---
title: Trabajar con celdas definidas por el usuario
type: docs
weight: 100
url: /es/java/working-with-user-defined-cells/
---
## **Leer celdas definidas por el usuario de las formas Visio**
 Los usuarios insertan campos de texto en formas para mostrar información adicional.**Celdas definidas por el usuario** es la única rama de estos campos y esta rama utiliza la información ingresada en la celda Valor de la sección Celdas definidas por el usuario en la ShapeSheet de la forma. Los desarrolladores pueden insertar y leer todas las celdas definidas por el usuario usando[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 La colección de Usuarios expuesta por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) La clase admite el objeto com.aspose.diagram.User. los[Usuario](https://reference.aspose.com/diagram/java/com.aspose.diagram/User) La clase se puede utilizar para leer propiedades. Hay algunas celdas definidas por el usuario como puede ver en la siguiente imagen:

**Tabla que muestra información sobre celdas definidas por el usuario** 

![todo:imagen_alternativa_texto](working-with-user-defined-cells_1.png)

El código siguiente se utiliza para leer celdas definidas por el usuario.

La siguiente imagen muestra el resultado después de ejecutar el código:

![todo:imagen_alternativa_texto](working-with-user-defined-cells_2.png)
#### **Ejemplos de programación**
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
### **Crear celda definida por el usuario**
El Aspose.Diagram for Java API permite a los desarrolladores crear celdas definidas por el usuario en la hoja de formas. Este tema de ejemplo describe cómo agregar tantas filas de nombre de usuario como sea necesario, asignar nombres significativos a las filas y establecer valores de celda.

El método add expuesto por la colección Users se puede usar para crear celdas definidas por el usuario en la hoja de formas. Toma un solo parámetro.

Use el siguiente código en su aplicación Java para crear una celda definida por el usuario en la hoja de formas usando Aspose.Diagram for Java.
#### **Ejemplos de programación**
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
## **Recuperar celdas definidas por el usuario de Shapesheet**
Aspose.Diagram for Java API permite a los desarrolladores recuperar celdas definidas por el usuario de la hoja de forma. Este tema de ejemplo describe cómo recuperar todos los nombres de usuario para todas las formas en un dibujo.
### **Recuperar celdas definidas por el usuario**
 Los métodos getNameU(), getValue().getVal() y getPrompt().getValue() expuestos por el[Usuario](https://reference.aspose.com/diagram/java/com.aspose.diagram/User)La clase se puede usar para recuperar celdas definidas por el usuario de la hoja de forma.
#### **Recuperar celdas de muestras de programación de Shapesheet**
Use el siguiente código en su aplicación Java para recuperar todas las celdas definidas por el usuario de la hoja de formas usando Aspose.Diagram for Java.
#### **Ejemplos de programación**
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
