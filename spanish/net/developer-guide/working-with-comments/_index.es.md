---
title: Trabajar con comentarios
type: docs
weight: 220
url: /es/net/working-with-comments/
description: Esta página describe cómo agregar o editar comentarios con la biblioteca Aspose.Diagram.
---
## **Agregue un comentario a nivel de página en el Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API permite a los desarrolladores colocar comentarios en cualquier lugar de la página de dibujo Visio.
### **Agregar comentario**
 El método AddComment, expuesto por el[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page) clase, permite a los desarrolladores agregar comentarios a una página de dibujo. Toma las coordenadas X e Y junto con una cadena de comentarios.
#### **Añadir comentario Ejemplo de programación**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.cs" >}}
## **Edite un comentario de nivel de página en el Visio Diagram**
 Microsoft Visio los usuarios agregan comentarios a toda la página que se presentan mediante un icono en la esquina superior izquierda de la página. Los desarrolladores pueden[añadir comentarios a nivel de página en el Visio](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API también admite modificar el comentario de nivel de página en Visio.
### **Editar comentario**
 La propiedad Comentario, expuesta por el[Anotación](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) clase, permite a los desarrolladores editar comentarios en la página de dibujo Visio.
#### **Editar comentario Ejemplo de programación**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.cs" >}}
## **Agregue un comentario de nivel de forma en el dibujo Visio**
[Aspose.Diagram for .NET](https://www.aspose.com/products/diagram/net)API permite a los desarrolladores agregar comentarios a la forma en un dibujo Visio.
### **Agregar comentario**
Un método AddComment sobrecargado, expuesto por el[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page)class toma una instancia de clase Shape y una cadena de texto del comentario.
#### **Añadir comentario Ejemplo de programación**
**C#**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// retrieve page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(12);

page.AddComment(shape, "Hello");

// save diagram

diagram.Save(@"c:\temp\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
