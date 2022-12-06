﻿---
title: Trabajando con Protección
type: docs
weight: 170
url: /es/net/working-with-protection/
description: Esta sección explica cómo configurar la protección en el diagram con Aspose.Diagram.
---
## **Establecer Protección del Visio Diagram**
 La protección de diagramas permite a los usuarios bloquear fondos, patrones (plantillas), formas y estilos para que no se puedan editar. Esto es útil para proteger los estilos corporativos, por ejemplo, y garantizar una apariencia coherente en un conjunto de diagramas. Los desarrolladores pueden lograr esto usando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Edite la protección Visio Diagram**
Las propiedades ProtectBkgnds, ProtectMasters, ProtectShapes y ProtectStyles, expuestas por el[Configuración del documento](http://www.aspose.com/api/net/diagram/aspose.diagram/documentsettings) La clase admite el objeto Aspose.Diagram.BoolValue. Estas propiedades se pueden utilizar para proteger y desproteger diagramas Microsoft Office Visio. En el Microsoft Visio proteges los documentos de esta manera:

1. Abra un diagram en Microsoft Visio.
1. Abra la ventana Explorador de dibujos.
1.  Haga clic derecho en diagram y seleccione**Proteger documento** del menú.
1. En la ventana Proteger documento, marque o borre las opciones para bloquear o desbloquear diferentes elementos diagram.
1.  Hacer clic**OK**.
#### **Edite la muestra de programación de protección Diagram**
Use el código a continuación en una aplicación .NET para realizar las mismas tareas, como bloquear y desbloquear diferentes elementos del Visio diagram usando Aspose.Diagram for .NET API.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Protection-VisioDiagramProtection-VisioDiagramProtection.cs" >}}
## **Establecer protección de la forma Visio**
 La protección de formas Visio permite a los usuarios bloquear aspectos específicos de las formas. Los aspectos de las formas que se pueden bloquear a través de la protección de formas incluyen el ancho, la altura, la posición x, la posición y, la rotación y más. Los desarrolladores pueden lograr esto usando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Edite la protección de forma Visio**
**Bloquear aspecto**, **LockBegin**, **BloquearCalcWH**, **BloquearRecortar**, **LockCustProp**, **BloquearBorrar**, **LockEnd**, **formato de bloqueo**, **LockFromGroupFormat**, **Grupo de bloqueo**, **Altura de bloqueo**, **BloquearMoverX**, **LockMoveY**, **Bloquear Rotar**, **BloquearSeleccionar**, **BloquearTextoEditar**, **LockThemeColors**, **Efectos de tema de bloqueo**, **BloquearVtxEditar** y**ancho de bloqueo** propiedades expuestas por[**Proteccion**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) apoyo de la clase**Aspose.Diagram.BoolValue** objeto. Estas propiedades se pueden utilizar para proteger y desproteger formas.

En Microsoft Office Visio, el usuario puede realizar las siguientes acciones para proteger cualquier forma:

- Abierto diagram en Microsoft Office Visio
- Seleccione cualquier forma
- Seleccione 'Protección...' en el menú 'Formato' si está usando Visio 2007 o seleccione 'Protección' en el menú 'Desarrollador' si está usando Visio 2010
- En la ventana 'Protección', marque/desmarque cualquier cuadro de texto para bloquear o desbloquear cualquier atributo de forma
- Presiona OK'
### **Edite el ejemplo de programación de protección de forma**
Use el siguiente código en su aplicación .NET para hacer lo mismo (bloquear/desbloquear cualquier atributo de forma) usando Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Protection-VisioShapeProtection-VisioShapeProtection.cs" >}}
