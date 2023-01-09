---
title: Trabajar con comentarios
type: docs
weight: 210
url: /es/java/working-with-comments/
---
## **Agregue un comentario a nivel de página en el Visio**
Aspose.Diagram for Java API permite a los desarrolladores agregar comentarios en cualquier lugar de una página del dibujo Visio.
### **Agregar comentario**
El método addComment, expuesto por la clase Page, le permite agregar comentarios a una página de dibujo. Toma las coordenadas X e Y junto con una cadena de comentarios.

 Microsoft Visio los usuarios agregan comentarios a toda la página que se presentan mediante un icono en la esquina superior izquierda de la página. Los desarrolladores pueden[añadir comentarios a nivel de página en el Visio](). [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API también admite modificar el comentario de nivel de página en Visio.
#### **Añadir comentario Ejemplo de programación**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.java" >}}
## **Edite un comentario de nivel de página en el Visio Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API admite la modificación del comentario a nivel de página en la página de dibujo Visio que se presenta mediante un icono en la esquina superior izquierda de la página.
### **Editar comentario**
La propiedad Comentario, expuesta por la clase Anotación, permite a los desarrolladores editar comentarios en la página de dibujo Visio.
#### **Editar comentario Ejemplo de programación**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.java" >}}
## **Agregue un comentario de nivel de forma en el dibujo Visio**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API permite a los desarrolladores agregar comentarios a la forma en un dibujo Visio.
### **Agregar comentario**
Un método addComment sobrecargado, expuesto por la clase Page, toma una instancia de la clase Shape y una cadena de texto del comentario.
#### **Añadir comentario Ejemplo de programación**
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
