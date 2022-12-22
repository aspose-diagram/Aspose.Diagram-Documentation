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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-User-defined-Cells-ReadUserdefinedCellsOfShape-ReadUserdefinedCellsOfShape.cs" >}}


Esta imagen muestra el resultado después de ejecutar el código anterior:

![todo:imagen_alternativa_texto](working-with-user-defined-cells_2.png)
## **Crear celda definida por el usuario en ShapeSheet**
[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/) permite crear celdas definidas por el usuario en la hoja de formas. Este tema de ejemplo describe la forma en que los desarrolladores pueden agregar tantas filas User.name como necesiten, asignar nombres significativos a las filas y establecer valores de celda.
### **Crear celda definida por el usuario**
El método Agregar expuesto por la Colección de usuarios se puede usar para crear una celda definida por el usuario en la hoja de formas. Toma un solo parámetro.
#### **Crear muestra de programación celular**
Use el siguiente ejemplo de código en su aplicación .NET para crear una celda definida por el usuario en la hoja de formas usando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-User-defined-Cells-CreateUserDefinedCellInShapeSheet-CreateUserDefinedCellInShapeSheet.cs" >}}
## **Recuperar celdas definidas por el usuario de Shapesheet**
Aspose.Diagram for .NET API permite recuperar celdas definidas por el usuario de la hoja de forma. Este tema de ejemplo describe la forma en que los desarrolladores pueden recuperar todos los User.name para todas las formas en un dibujo.
### **Recuperar celdas definidas por el usuario**
Las propiedades NameU, Value.Val y Prompt.Value expuestas por la clase User se pueden usar para recuperar celdas definidas por el usuario de la hoja de forma.
#### **Recuperar celdas de muestras de programación de Shapesheet**
Use el siguiente código en su aplicación .NET para recuperar todas las celdas definidas por el usuario de la hoja de formas usando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-User-defined-Cells-RetrieveUserDefinedCells-RetrieveUserDefinedCells.cs" >}}
