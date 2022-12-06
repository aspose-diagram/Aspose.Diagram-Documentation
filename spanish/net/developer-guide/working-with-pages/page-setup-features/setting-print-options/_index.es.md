---
title: Configuración de las opciones de impresión
type: docs
weight: 10
url: /es/net/setting-print-options/
description: Esta sección explica cómo configurar las opciones de impresión con Aspose.Diagram.
---
{{% alert color="primary" %}}

A veces, es necesario configurar los ajustes de configuración de página para que las páginas controlen la impresión. Estos ajustes de configuración de página ofrecen varias opciones.

{{% /alert %}}

## **Configuración de las opciones de impresión**

Las opciones de configuración de página son totalmente compatibles con Aspose.Diagram. Este artículo explica cómo configurar las opciones de página con Aspose.Diagram y muestra ejemplos de código para configurar:

 Aspose.Diagram proporciona una clase,[**Página**](https://reference.aspose.com/diagram/net/aspose.diagram/page) , que representa un archivo Microsoft Visio. los[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) la clase contiene un[**Paginas**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) colección que permite el acceso a cada página en el archivo Visio. Una página está representada por el[**Página**](https://reference.aspose.com/diagram/net/aspose.diagram/page)clase.

 los[**PáginaHoja**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) la clase proporciona la[**ImprentaAccesorios**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) propiedad que se utiliza para establecer las opciones de configuración de página de la página. De hecho, esto[**ImprentaAccesorios**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) La propiedad es un objeto de la[**PáginaHoja**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) clase utilizada para establecer diferentes opciones de diseño de página para una página impresa. los[**ImprentaAccesorios**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)class proporciona varias propiedades que se utilizan para establecer las opciones de configuración de la página. Algunas de estas propiedades se analizan a continuación.

### **Orientación de la página de impresión**

 La orientación de la página de impresión se puede establecer en vertical u horizontal mediante el[**ImprentaAccesorios**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) clase'[**ImprimirOrientaciónPágina**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) propiedad. los[**ImprimirOrientaciónPágina**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) propiedad acepta uno de los valores predefinidos en el[**ValorOrientaciónPáginaImprimir**](https://reference.aspose.com/diagram/net/aspose.diagram/printpageorientationvalue)enumeración, que se enumeran a continuación.

|**Tipos de orientación de la página de impresión**|**Descripción**|
|:- |:- |
|MismoComoImpresora|Igual que la orientación de la impresora|
|Paisaje|Orientación horizontal|
|Retrato|Orientación Vertical|

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPageOrientation-SetPageOrientation.cs" >}}

### **Factor de escala**

 Es posible reducir o aumentar el tamaño de una página ajustando el factor de escala con el[**EscalaX**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/scalex)propiedad.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPageOrientation-SetPageScale.cs" >}}
