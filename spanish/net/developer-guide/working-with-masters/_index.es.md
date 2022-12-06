---
title: Trabajando con Maestros
type: docs
weight: 70
url: /es/net/working-with-masters/
description: Esta sección explica cómo agregar maestro u obtener información maestra con Aspose.Diagram.
---
## **Recuperación de información maestra**
Un patrón de forma es otro nombre para una plantilla Visio. Con Aspose.Diagram, es posible recuperar información sobre páginas, conectores y también maestros. Este artículo explica cómo obtener el ID y el nombre de un diagram.

 los[Maestro](http://www.aspose.com/api/net/diagram/aspose.diagram/master) objeto representa un[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) maestro del objeto en un diagram. La propiedad Masters, expuesta por la clase Diagram, admite una colección de objetos Aspose.Diagram.Master. Esta propiedad se puede utilizar para recuperar la información de los maestros, es decir, el ID y el nombre del maestro. Utilice la propiedad Page.Shapes para determinar qué forma ha heredado la forma maestra.
### **Muestra de programación de recuperación de información maestra**
El siguiente fragmento de código recupera la información maestra de un diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-RetrieveMasterInfo-RetrieveMasterInfo.cs" >}}
## **Agregar maestro desde la plantilla de formas**
Una plantilla es una colección de formas asociadas con una plantilla Microsoft Office Visio particular. Con Aspose.Diagram, es posible agregar cualquier patrón de forma a un dibujo desde una plantilla.
### **Agregar maestro**
 los[Maestro](http://www.aspose.com/api/net/diagram/aspose.diagram/master) objeto representa un[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) maestro del objeto en un diagram. El método AddMaster, expuesto por la clase Diagram, permite agregar un maestro desde una plantilla. Ofrece las siguientes cuatro formas:

- Ruta del archivo de plantilla e ID principal.
- Ruta del archivo de plantilla y nombre principal.
- Secuencia de archivo de plantilla e ID maestro.
- Flujo de archivo de plantilla y nombre maestro.
- Agregar maestro a diagram desde la fuente diagram
#### **Agregar muestra de programación maestra**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-AddMasterFromStencil-AddMasterFromStencil.cs" >}}
## **Crear maestro desde cero**
 Aspose.Diagram API permite crear un[Maestro](http://www.aspose.com/api/net/diagram/aspose.diagram/master) desde cero sin ningún stencil, dibujo o plantilla. Los desarrolladores pueden personalizar la creación de Master. El método AddMaster, expuesto por la clase Diagram, permite agregar un maestro.
### **Crear muestra de programación maestra**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-CreateMasterFromScratch-CreateMasterFromScratch.cs" >}}
## **Obtenga un Máster del Archivo Visio**
A veces, los desarrolladores necesitan obtener los detalles del maestro de un dibujo Visio. El Aspose.Diagram API admite esta función.

 Aspose.Diagram for .NET ofrece la[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)clase que representa un dibujo Visio. La propiedad Masters, expuesta por la clase Diagram, admite una colección de objetos Aspose.Diagram.Master. Esta propiedad se puede utilizar para recuperar los detalles de un maestro en particular. La clase MasterCollection expone los métodos GetMasterByName y GetMaster a los que se puede llamar para obtener un objeto Master.
### **Obtener un objeto maestro por ID**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Llame al método GetMaster de la clase Diagram.Masters.
#### **Ejemplo de programación de objeto maestro por ID**
El siguiente ejemplo muestra cómo obtener un maestro por ID de un dibujo Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyID-GetMasterbyID.cs" >}}
### **Obtener un objeto maestro por nombre**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Llame al método GetMasterByName de la clase Diagram.Masters.
#### **Ejemplo de programación de objeto maestro por nombre**
El siguiente ejemplo muestra cómo obtener un objeto maestro por nombre de un dibujo Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyName-GetMasterbyName.cs" >}}
## **Compruebe la presencia de un maestro en el dibujo Visio**
El Aspose.Diagram API admite la comprobación de la presencia de un maestro en un dibujo Visio. Con la propiedad MasterCollection, los desarrolladores pueden verificar si un maestro está presente por su nombre o ID.

 Aspose.Diagram for .NET ofrece la[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase que representa un dibujo Visio. La propiedad Masters, expuesta por la clase Diagram, admite una colección de objetos Aspose.Diagram.Master. Esta propiedad se puede utilizar para comprobar la presencia de un maestro en particular. La clase MasterCollection expone el método IsExist al que se puede llamar con el nombre maestro o el parámetro ID.
### **Comprobación de una presencia maestra por ID**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Llame al método IsExist de la clase Diagram.Masters.
#### **Ejemplo de programación de Master Presence by ID**
El siguiente ejemplo muestra cómo verificar la presencia de un maestro por ID en un dibujo Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyID-CheckMasterPresencebyID.cs" >}}
### **Comprobación de la presencia de un maestro por nombre**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Llame al método IsExist de la clase Diagram.Masters.
#### **Ejemplo de programación de presencia maestra por nombre**
El siguiente ejemplo muestra cómo verificar la presencia de un maestro por nombre del dibujo Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyName-CheckMasterPresencebyName.cs" >}}
