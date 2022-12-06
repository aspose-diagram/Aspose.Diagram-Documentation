---
title: Trabajar con capas
type: docs
weight: 130
url: /es/net/working-with-layers/
description: Esta sección explica cómo agregar u obtener información de capa en una forma visio con Aspose.Diagram.
---
## **Configurar objetos de forma con capas en Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) permite configurar objetos de forma con capas en Microsoft Office Visio diagram. Cada forma puede pertenecer a varias capas para que los desarrolladores puedan administrar las formas para satisfacer las necesidades del usuario final. los[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) El objeto de clase ofrece la propiedad LayerMember que permite agregar y eliminar objetos de forma hacia y desde las capas en el dibujo Visio. Los usuarios pueden administrar estas propiedades mediante programación usando Aspose.Diagram API de la siguiente manera:
### **Configurar muestra de programación de objetos de forma**
El siguiente fragmento de código ayuda a agregar, eliminar y mover propiedades de objetos de forma.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-ConfigureShapeLayers-ConfigureShapeLayers.cs" >}}
## **Agregue una nueva capa en el Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) permite a los desarrolladores agregar nuevas capas para organizar categorías personalizadas de formas y luego asignar formas a esas capas mediante programación. los[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) La clase ofrece el método Add que permite agregar un nuevo[Capa](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) en el dibujo Visio. Los desarrolladores pueden establecer las propiedades de la capa inicializando su objeto de clase.
### **Agregar muestra de programación de capas**
El siguiente fragmento de código ayuda a agregar objetos de capa.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-AddLayer-AddLayer.cs" >}}
## **Recuperar todas las capas del Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) da acceso a los desarrolladores para obtener las capas existentes de un Visio diagram. El[PáginaHoja](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) propiedad de la[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class permite recuperar la lista de capas disponibles de un Visio diagram usando[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) clase.
### **Ejemplo de programación de recuperación de capas**
El siguiente fragmento de código ayuda a obtener la lista de capas.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-RetrieveAllLayers-RetrieveAllLayers.cs" >}}
