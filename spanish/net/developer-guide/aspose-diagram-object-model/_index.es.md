---
title: Aspose.Diagram modelo de objeto
linktitle: Aspose.Diagram modelo de objeto
type: docs
description: El modelo de objetos Aspose.Diagram proporciona información sobre las relaciones estructurales entre los objetos de la biblioteca de clases Aspose.Diagram.
weight: 20
url: /es/net/object_model
---
{{% alert color="primary" %}} 

**Aspose.Diagram modelo de objeto**

El modelo de objetos Aspose.Diagram proporciona información sobre las relaciones estructurales entre los objetos de la biblioteca de clases Aspose.Diagram.

{{% /alert %}} 

### La estructura de nivel superior del modelo de objeto Aspose.Diagram se muestra a continuación de forma jerárquica.

|**Estructura de nivel superior del modelo de objeto Aspose.Diagram**|
|:- |
|![Estructura de nivel superior del modelo de objeto Aspose.Diagram](diagram-classes.png)|

Como puede ver en la figura anterior, la raíz del modelo de objeto es el objeto Diagram. A continuación se proporciona una breve descripción de algunos de los objetos con fines introductorios.

#### **Colección de páginas/Página**

El objeto Diagram contiene PageCollection, que representa la colección de todos los objetos de página en un Diagram.

#### **ShapeColección/Forma**

El objeto de página contiene ShapeCollection, que representa la colección de todos los objetos de forma en una página. El objeto de forma contiene elementos que definen una forma en un elemento de forma maestro, página o grupo.

#### **ConectarColección/Conectar**

El objeto de página contiene ConnectCollection, que representa la colección de todos los objetos de conexión en una página. El objeto Conectar representa una conexión entre dos formas en un dibujo, como una línea y un cuadro en un organigrama.

#### **StyleSheetCollection/StyleSheet**

Representa un estilo definido en un documento.

#### **MasterCollection/Master**

Contiene elementos que definen un maestro para el documento. Un maestro es una forma en una galería de símbolos que usa repetidamente para crear dibujos. Cuando arrastra una forma desde una galería de símbolos a la página de dibujo, la forma se convierte en una instancia de ese patrón y se incluye una copia local del patrón en el documento.

#### **Propiedades del documento**

Contiene elementos de propiedad del documento, como el título del documento, el autor, etc.

#### **EncabezadoPie de página**

Contiene elementos para el encabezado y pie de página de un documento.

#### **Proyecto Vba**

Representa el proyecto VBA.

#### **TemaColección/Tema**

El tema dinámico define propiedades que especifican propiedades de color, fuente, relleno, propiedades de línea y efecto.

#### **Llenar**

Contiene los valores de formato de relleno actuales para la forma y la sombra paralela de la forma, incluido el patrón, el color de primer plano y el color de fondo.

#### **Línea**

Contiene elementos que controlan los atributos de línea de una forma, como el patrón, el grosor y el color. Estos elementos determinan si los extremos de las líneas tienen formato (por ejemplo, con una punta de flecha), el tamaño de los formatos de los extremos de las líneas, el radio del círculo de redondeo aplicado a la línea y el estilo de la tapa de la línea (redondo o cuadrado).

#### **geomas**

Contiene una colección de elementos Geom.

#### **Caracteres**

Contiene una colección de objetos Char que contiene estilos de texto de la forma.

#### **Texto**

Contiene el texto de una forma.

#### **Formulario X**

Contiene elementos que especifican información de posicionamiento general sobre una forma.

#### **TextoXForm**

Contiene elementos que especifican información de posicionamiento sobre el bloque de texto de una forma.

#### **Colección de hipervínculos/Hipervínculo**

El objeto de hipervínculo contiene elementos para crear varios saltos entre una forma o una página de dibujo y otra página de dibujo, otro archivo o un sitio web.

#### **MasterShape**

Este atributo solo puede estar presente en formas que son miembros de una forma de grupo, y el grupo es una instancia de un maestro. El atributo contiene un ID que hace referencia a la subforma correspondiente en el maestro.

#### **FieldCollection/Field**

El objeto de campo contiene elementos que especifican funciones y fórmulas insertadas en el texto de la forma.
